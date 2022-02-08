# Solo Project: Spike

Your solo project is going to require you to accomplish something you've never done before. There is some part about it (complicated SQL queries, an API you haven't worked with before, payments, image upload, task scheduling, sending email/text messages, etc) that is probably a little intimidating.

- Check out this list of [Common Solo Project Technologies in React](https://github.com/PrimeAcademy/prime-solo-common-tech), for some ideas of what previous students have used to tackle some of these problems.

- Submit in the portal a brief description of what you plan to spike before you leave. (You dont have to have the repo made yet)

- Create a spike (very small example) that will serve as a "Proof of Concept" for this really hard part of your project.

> Note: __DO NOT__ use the solo project starter repo! You want to keep this as simple as possible to focus on the new part.

- Submit the GitHub link to your repo in the portal.


## Summary of what I did 

This whole project is basically spike. I'm surprised I built as much as I did given how intimidated/terrified I was this whole week prior. 

The most working reliable tonejs code I could find was in the tonejs examples page on tonejs.github.io. They stored all their js functionality in script tags, so I was able to steal a lot of it by keeping the chrome inspector up on my second monitor and typing stuff out. Surprisingly it only took a few simple imports to get stuff working in plain html. It was pretty much a matter of picking apart examples that I liked and chunking them together based on what I put in my scope doc. The js part was easy enough, it was those darn tonejs html tags that gave me trouble, particularly the sequencer. 


I started off by copying the step sequencer from the examples page. Like I said, my biggest gripe was building out the HTML because I had to map out every column and every cell of the thing, plus the weird bpm slider, thankfully there was styling built into one of the imports. I was able to turn it into a drum machine by changing the baseurl to a drum samples folder. A lot of these examples read audio off a server which links you to different sample folders depending on which part of the URL you visit. Needless to say, I downloaded a buncha cool samples from there. 

Next came the fx sends. I stole these from the Busses section of the tonejs examples. Was a similar process of building out the html and mapping out the js accordingly. I was kinda surprised by how easy it was to turn a reverb send into a pingpong delay send, all I had to do was change some names around. I later added a tone drawer (drawer().add({})) which builds out controls for each fx component. 

I'm sorta seeing tonejs as a funny mix of jquery and cSound. 

Next came this funny little polysynth. As you can probably guess, I took the bulk of this code from the poly synth section of the examples page. This part of the process was really funny because I spent about an hour busting my ass building out this gigantic html piano, only to realise that the js piano object builds out the whole darn thing for you. I laughed for a couple minutes, then got back to work. once I got the synth playing alongside the drum machine I changed it to an fm synth, then added a limiter and a reverb send. 

I was happy with the thing I made so I made some drum sounds moved some sliders, changed some params around, and jammed out a bit. 

After jamming a bit, I cleaned up the code a tad and added mock-up buttons for saving and loading presets, plus a random button that I hope to get to. 

I'm happy enough with how this app sounds, the one thing I couldn't figure out is how to save presets to a database or how to randomize the sequencer. The synth and effects components are formatted with json (visible in each component), but the send/bpm sliders and step sequencer are all in html state. React might help with this. Or it might make things more confusing. It's definitely possible, just gonna take some finagling. I'm a lot less worried than I was a week ago. 
