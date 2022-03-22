This web was made by Gerard Ramon(Kramtron on GitHub),Spanish student of CITM,UPC, this is a personal research with the objective of explain how to do a good dialog system and how to introduce it into the rpg.




# Introduction




# What is a dialog system?
It is the way to emulate a conversation between the player and a character controlled by the machine (NPC).
Normally they are predefined phrases by the creators of the video game that depending on the moment are loaded on the screen to show them to the player.


![](https://media.moddb.com/cache/images/games/1/49/48640/thumb_620x2000/New_dialogue_system.png)

 *Divinity: Originals Sin II


# Different dialog systems

![](https://i.stack.imgur.com/yig2q.png)
![](https://dk135eecbplh9.cloudfront.net/assets/blt040e3727e9b40f23/DialogTreeStructure.png)
![](https://i.stack.imgur.com/Krwdk.png)

## Non-Branching Dialogue

In games using non-branching dialogue, the simplest form of interaction, the player walks up to an NPC and initiates conversation. The NPC delivers his or her lines and the conversation ends. Alternately, initiating a conversation with an NPC triggers a cutscene where the player's avatar and the NPC have a non-interactive dialogue.

If the player talks to the same NPC again after certain events, the NPC may have different things to say, but the player never has any control over the conversation. The only decision-making involved is whether or not to talk to the NPC.

This type of interaction is extremely common and easy to implement, and can therefore be seen in almost any game featuring non-hostile NPCs, such as the original Final Fantasy and The Legend of Zelda: Ocarina of Time. While non-branching dialogue is still a regular facet of modern games, due to the absence of gameplay it is included in this article only for reference.

## Branching Dialogue

Game dialogue becomes more interactive when conversations can take different paths. The player reads dialogue and chooses their response from a limited set of choices available to them. Conversation typically moves forward such that the player cannot go back to previous topics or responses.
From this basic framework, NPC interaction can be as simple as the player answering a yes or no question in a three-line conversation with a random NPC in town, or as complex as the relationship-building simulations in Japanese dating games like Tokimeki Memorial.

In games where branching dialogue is the primary gameplay focus, the player's choices often affect the NPCs' attitudes toward the player one way or another, with the player attempting to guess the "best" response in order to maximize NPC disposition.

One common technique employed to give the player a greater illusion of freedom is to have multiple responses lead to the same path. This is usually done as an attempt to limit the quantity of dialogue that must be produced for the game. Therefore, branching dialogue usually curves back in on itself such that while an individual choice may immediately produce a unique response, the rest of the conversation is typically not unique to that choice.

In games where the goal of conversation is to improve the player's relationship with the NPC, however, while every choice may not change the course of the dialogue, each choice may have a different number of "mood points" associated with it, and thus the player must still carefully consider his options at every turn.

An interesting variation in branching dialogue, found in the game Culpa Innata, sees the player choosing one of several tactics at the beginning of the conversation. For example, while interviewing a potential witness in a crime, the player chooses to use either a formal, casual, or accusatory manner.

This decision affects the tone of the conversation, the options, and, ultimately, the information gleaned from the interviewee. Some tacts are more successful than others, and the player cannot immediately go back and try a different method. In order to approach the conversation differently, the player must come back another day.

The interface used by the player in branching dialogue varies significantly from game to game. The most obvious method is to present the player's possible responses word-for-word as his or her avatar would say them. The player has an infinite amount of time from which to make his decision, and the NPC gives his or her reaction as soon as the player makes his choice.

This is the case with most dating simulations and many western RPGs like Planescape: Torment. There is no ambiguity in the player's decision, but reading all the possible responses takes time and brings conversation flow to a halt.

While this is not necessarily a problem in games featuring dialogue presented entirely in text, modern games typically present all dialogue with full voice acting. As a result, the menu navigation and long pauses while the player chooses their next response can negatively impact immersion.

Games have attempted to address this issue by presenting responses in a different manner, or controlling the speed at which the player responds. In some cases, designers choose to present full responses alongside symbols or text that quickly sum up the general gist of the response.

An example of this technique can be seen in Desperate Housewives: The Game (Liquid Entertainment 2006). The game presents the player's options as a series of stylized faces depicting various emotions associated with the response, such as happy, sad, or angry. When the player moves their mouse over one of the faces, the full response appears in a text bubble for the player to read if they wish.
If the player knows they want to respond to a particular comment in a negative manner, they can quickly filter out the responses they do not want and just read the angry choices, thereby reducing the load on the player and speeding up dialogue to a more natural level.

One game notable for its aspirations for cinematic-quality dialogue scenes is Indigo Prophecy, which eliminates full responses entirely. The player sees his choices pared down to their essence, such as "Lie", "Avoid the question", or "Ask about murder weapon."

Once the player decides, his avatar delivers the full line related to the player's choice. In addition, the player has only a limited time in which to make a decision after the NPC finishes speaking. If the player fails to make a decision in that time, the game chooses a response for them, in a deliberate attempt to keep the conversation moving at a more natural pace.

# XML use in dialog systems
-Have all the phrases written so you only have to load them when necessary.

-Remember the options that the player has taken.

-To be able to modify the name of the player.

-Code data

By following the basic structure and order we can improve comfort when working with large amounts of text. At the same time that will help us to work with greater speed.

# How to print characters on screen?

We use SDL_TTF to conveniently and quickly print different characters on the screen.

![](https://lispbuilder.github.io/documentation/ttf-hello-world.png)

## How is it implemented?

### Step 1-Initialize
![](https://raw.githubusercontent.com/kramtron/Dialog-System/main/img/1.png)

### Step 2-Load font
![](https://raw.githubusercontent.com/kramtron/Dialog-System/main/img/2.png)

### Step 3-Render Text
![](https://raw.githubusercontent.com/kramtron/Dialog-System/main/img/3.png)

### Text Input
![](https://raw.githubusercontent.com/kramtron/Dialog-System/main/img/4.png)

### Delete
![](https://raw.githubusercontent.com/kramtron/Dialog-System/main/img/5.png)
# What problems does SDL_TTF have?

The problem is clear, it has memory leaks.
Creating a code that does the same for you may be the solution, but it is not something easy or short to do.
