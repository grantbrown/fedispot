# fedispot

A proposed scheme (and maybe software?) for allowing ham radio "spotting" on top of mastodon. Currently just some very scattered thoughts, especially since I’ve never really gotten into micro-blogging before. 

# License

Public domain. Lol. 

# Goals

The goal of this specification is to define a way in which Mastodon can be used by radio amatures in a fairly organic way to announce various types of activations, while permitting automated [spotting](https://worldradioleague.com/spotting-feature-guide/) as well as visualization of said spots by third party clients. 

More specifically, two directions of use should eventually be possible:

1. Someone posts a toot with particular hash tags, which would be able to be picked up by a spotting service of some sort, using their regular Mastodon interface. The hash tags need to offer a simple, minimal interface. Replies to the original toot should also be able to pick up changes or additional information – QSY, QRT, etc. 
2. The specification should allow other software to use the Mastodon API to generate toots of the appropriate format.

In this way, spotting could be integrated with the other social aspects of Mastodon (posting images, notes, chatting, following particular activators etc.)

# Structure


The proposed structure is organized hierarchically, with each level imposing additional required elements in order to be appropriately processed. The following is an incomplete look at the potential organization of the collection of hashtags. 

## A. Universal Required Elements

1. Invocation – some indication that fedispot should recognize the activation. Could be a hashtag or @ for a bot. 
2. Callsign (or an alternative registration mechanism)
3. Frequency (KHZ)

## B. Activity Groups

1. (generic) – no activity specified
2. POTA
3. SOTA
4. WWFF

## C. Detail Elements

Detail elements will be nested within activities (with the default activity including a set of very commonly used elements. Elements will include things like:

1. Mode
2. Specific entities (format will vary, like POTA parks or given summits)
3. Special events

## D. Dynamic Elements

Generally expected in replies or self-replies:

1. QSY
2. QRT
3. Re-spot
