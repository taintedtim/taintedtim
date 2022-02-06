# the ultimate guide to UIBlox

UIBlox is Roblox's system for managing & creating UI's (basically). It's been used for a while, and all of their core scripts are gradually being switched to it. So naturally, the first question the pops into your head would be: "how the ### do I use this?!"

And the answer will most likely be "I don't know, who do you think I am?". But not today. Because believe it or not, the minds here at taintedtimthisisnotarealcompanytm have figured it out. Okay anyways here's how to do it.

# install rojo

Firstly, you want to import the core packages. Now, you may be asking, how do I do that? Well, my lucky friend, here's how.

Luckily, rojo makes this easy for us. Since Roblox's CorePackages were actually *made* in Visual Studio Code & imported with rojo - it's incredibly easy. First, install the VS Code extension for rojo.

https://marketplace.visualstudio.com/items?itemName=evaera.vscode-rojo

Once you've installed that visual studio code plugin (and I hope visual studio code), we can go on to the next step. Search for Roblox Player on your PC, like so (if you're not using Windows then too bad haha):

# get the core packages

![searching for it](images/search.png)

Next, right click the item and press **Open file location**.

![press that lol](images/ofl.png)

Now, you're in the folder that most likely has Roblox & Roblox Studio. Right click Roblox Player, and press Open file location (again).

![press that lol x2](images/ofl2.png)

You're *finally* in the Roblox folder. From there, open up ExtraContent.

![open it](images/extracontent.png)

Inside of ExtraContent, there will be a folder called LuaPackages. Right click it, and press Copy.

![copy the thingy](images/copyec.png)

# set up the project

From there, make a new folder somewhere on your computer. Then, open it up in VS Code.

![making alt things is boring](images/openfolder.png)

![fffffffffffffffffffffff](images/yesclickyes.png)

You *may* see a popup seeing if you trust the authors of this. Just click that blue button, because I'm assuming you trust yourself.

![click it click the button](images/itrustme.png)

Assuming you have the Rojo VS Code plugin installed, press Ctrl+Shift+P and then type Rojo: Initialize. Press enter.

![k](images/fghj.png)

You should see something called default.project.json was created. Remove everything that's inside of it, and paste this in instead.

```json
{
  "name": "corepackages",
  "tree": {
    "$className": "DataModel",

    "ReplicatedStorage": {
      "$className": "ReplicatedStorage",
      "Common": {
        "$path": "src/shared"
      }
    }
  }
}
```

Your `default.project.json` should now look like this:

![idk](images/oops.png)

With all of that out of the way, remove every inside the `src` folder and make a folder inside of `src` called `shared`. Your setup should look like this:

![hamilton](images/uhohyoumadethewrongsuckeracuckold.png)

*note: <a href="#get-the-core-packages">since you had to copy the json to your clipboard you have to re-copy LuaPackages. please do that</a>*

Inside of `src/shared`, paste LuaPackages in.