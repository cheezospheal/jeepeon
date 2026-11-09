# Jeepeon
A 3D-printable figure of a Jolteon riding in a Jeep to keep you company!

I originally joined Half Life because I wanted to make 3D-printable art toys! I've seen so many on social media (particularly from svvart and BlakeMakes) and they always look super cool. I've always loved to draw and create art, and creating these art toys was just something I wanted to learn how to do. I've also always been a fan of figures, specifically those that come in blind boxes, and I even have my own Jolteon figure! Still, I thought it'd be super cool to make my own custom one. I'll just say that those videos on Youtube made it look much easier than it actually was... When deciding what to sculpt, it was partially based off the Jolteon figure I already own and also my own profile picture (on Github, Slack, Discord...). I LOVE this profile picture and I use it everywhere, so it's almost become part of what people recognize me as (just ask people in #half-life!). It's super cute but still complex enough to give me a little bit of a challenge.

<img width="500" alt="Screenshot 2026-11-08 020559" src="https://github.com/user-attachments/assets/f55570fa-1902-4eb3-8e3f-3c5db56db2b0" />

## Summary
This 3D model was designed in **Blender** and it was made printable using **BambuStudio**. If you want to edit anything, download and import the respective softwares and files.
|File|What's Inside?|
|---|---|
|jeepeon.blend|contains the editable Blender file|
|jeepeon.3mf|contains the 3mf file|
|jeepeonprint.3mf|contains the printable 3mf file, including its arrangement & supports|
|BOM.csv|Bill of Materials (this is for Half Life only, please refer below for users)|

Additionally, for reference, here is the image I based my model off of:

<img width="500" alt="jeepeon" src="https://github.com/user-attachments/assets/6f88d465-c58d-4ef1-a569-d45950f1921f" />

<br><br>
If you would like to make any changes to the model, I recommend turning on the following settings, which will just make it easier:
* Edit -> Preferences -> Get Extensions -> 3D Print Toolbox (this will make it easier to see and fix errors with 3D printing your model)
* Edit -> Preferences -> Get Extensions -> 3MF Import/Export (this will allow you to import/export the 3MF for printing)
* Edit -> Preferences -> Navigation -> Depth (this will allow you to zoom in as much as you want)
* Viewport Overlays -> Face Orientation (this will allow you to see the orientation of your normals, they should all be grey if they are correctly oriented)
* Edit -> Preferences -> System -> Undo Steps (this will allow you to increase the amount of undo history you have. Blender takes absolutely everything, including even selecting a part, as something that can be "undone", so it's best to have a high undo history so you can undo a change you later regret)

## Features
* A modeled low-poly jeep design
* Jeep details, such as wheels, steering wheel, rearview mirrors, grills, trim, and seat
* A low-poly Jolteon model with detachable ears, collar, and torso
* Fully manifold/watertight parts, sliced and with supports (ready for printing)!

The dimensions are approximately 17cm x 17cm.

## Jeep
Since I'm a beginner in Blender, I wanted to use a tutorial to make the Jeep part of my model. The tutorial I used was: https://www.youtube.com/watch?v=1n_lmuEQyZM, however it is also important to note that it may be inaccurate if you are using Blender 4.0+. Additionally, this tutorial is best used to make a video game model rather than a 3D-printable model (you'll see why later on), so the tutorial is best used as a reference rather than a copy-paste. It also basically doesn't look anything like my Jeep, so I mostly used it to learn some basic keybinds and tools (such as S for scale or G for grab) rather than actually making it. I recommend the same for any Blender tutorial you wish to use, since you don't know exactly what they'll be using it for (there are separate requirements for a render, video game model, or 3D printable model), and be creative so you don't just copy the tutorial word for word! 

<img width="300" alt="image" src="https://github.com/user-attachments/assets/539db9d2-7a71-417e-b756-9b59945943fb" />

For example, some changes I made were adding the grills, headlights, windshield, seat, and trim, as well as changing the shape of the car entirely. Blender is very customizable, and you won't risk your project accidentally breaking or not working.

## Jolteon

<img width="300" alt="image" src="https://github.com/user-attachments/assets/04880d6f-0ea0-47db-93e5-1bfdab858ad4" />

### Body
While the Jeep was made using basic shapes and tools (extruding, inset, etc.), the Jolteon was mostly made using Sculpt since it's an organic shape. To learn some basic sculpt tools, I recommend the tutorial https://www.youtube.com/watch?v=Lxem4yMs5Dg. Like before, it's more useful for learning the tools rather than applying them so I wouldn't bother with the starter project unless you're really struggling. Most of the tools in Sculpt are intuitive anyways, and I basically only used 3 tools - clay strips, smooth, and snake hook. Clay strips are to add and remove general shapes, smooth is to smooth out the geometry, and snake hook is to add and stretch out the clay. Another thing I'd recommend is only making things with sculpt that you absolutely need to sculpt (i.e., they are organic shapes). For example, the ears can just be made by extruding out a flat shape. Don't make things harder for yourself than necessary! 

### Ears & Collar
Like I said before, only make things you need to with sculpt. For the ears and collar, I didn't make them with sculpt since they can pretty easily be made geometrically. For these, I used a technique called "vertex tracing", or when you basically trace out a polygon and extrude it. To do this, you need to make a plane, merge all its vertices into the center, move the vertex, and extrude the vertex to create the shape. You can make any polygon you want, but I just traced out the ears and collar in my reference image so I could just extrude them. Reminder that, when tracing, you want to have a flat view and to not change it when tracing, as this will cause changes in the depth. You'll need to press one of the keys on your numpad to get into a preset view. Another thing I recommend is turning out vertex snapping and merging, which you can do so by clicking the magnet icon in the top bar. This'll make it so that, when you create your polygon, the last vertex will merge together with your start vertex and actually create a closed shape. 

## Getting Ready to Print
Blender isn't just for 3D printing. It can be used for video game modeling, rendering, art, etc. So, Blender often allows you to make changes that won't be allowed when 3D printing, but will be allowed for other uses. However, this project is meant to be printed, so there are some requirements that must be met. To check if they have been met, you can either check manually (very difficult) or check with the free extension 3D Print Toolbox (see Summary). It'll tell you all the errors and where they're located, much like the DRC in KiCad. Here are the errors that I had and how I fixed them, though I recommend just searching up how to fix the other ones (or of course, using trial and error until it works):

### Non-Manifold Edges
<img width="294" height="703" alt="image" src="https://github.com/user-attachments/assets/a2626be7-5fde-4074-9004-bbd75139f992" /> <br>
(these non-manifold edges were created because I made my Jeep with a mirror modifier, so there's an open face/hole within those edges)

This is the most common error, and it basically means that there are edges that create holes in your model, so it isn't just one solid form. Your print will therefore also come with holes. It really depends on why the edges were caused, but you can fix them by either filling in the holes using F, merging together the edges using M, or using a Boolean Unify modifier. You can also just use the Clean Up -> Make Manifold in the 3D Print analyzer, but that doesn't work all the time, so I personally think it's better just to do it manually since the Make Manifold also often creates other errors (I fixed all my errors manually). Sometimes, there'll also be some edges you can't see that are somehow non-manifold, but you can just Select -> Select All by Trait -> Non-Manifold and just delete those. Generally they're easy to fix, but again, it really depends on the situation that they have been created!

### Intersect Faces

<img width="228" height="193" alt="image" src="https://github.com/user-attachments/assets/4a0a9e21-bf7e-44b0-bdc7-8c654031c1e2" /> <br>
(these intersect faces were created because the arm of the rearview mirror is inside the car)

This is the second most common error, and there's no real way to fix it (at least to my knowledge, which is little) It's created by having faces inside other faces, and is most common when you join together two parts. You can't have two parts inside each other, and they won't be read as just the outside faces. You can either remesh it or use a Boolean Difference modifier. Remeshing will essentially make your multiple parts read as just one mesh, but it often makes your mesh look kind of unnatural since it'll have a set voxel size, especially if your model is low-poly like mine. Using a Boolean Difference modifier will make it so that your parts will perfectly fit together rather than being inside each other, but it'll make it so they are separate parts that need to be glued together once printed. It is best used for parts that you can easily glue on, such as the wheels or the rearview mirrors. 

<img width="228" alt="image" src="https://github.com/user-attachments/assets/f8898355-136f-421c-8f25-f3a2a7525753" />

### Zero Faces

<img width="663" height="559" alt="image" src="https://github.com/user-attachments/assets/1d123f1e-132f-4200-a5bc-af089dbfbd5e" /> <br>

Zero faces are faces with an area of zero. Again, I'm not too sure exactly how to fix it, but this is what worked for me. Additionally, they're also pretty uncommon. The zero faces in my model were created because one part of my mesh that was beveled was connected to another part of a mesh that wasn't, so the connecting area of the bevel faces and the vertex below it created a face that had no area. To fix it, all I had to do was merge together the vertices of the zero face into one vertex.

### Non-Flat Faces
<img width="200" height="197" alt="image" src="https://github.com/user-attachments/assets/ee95f6e3-c0a2-481e-9ce7-1547d41f2c40" /> <br>

Non-Flat faces are self-explanatory. To fix them, you have to triangulate your faces. This can also be done in BambuStudio or another applicable software, since most can only read in triangles anyways. However, to make them into triangles in Blender, either use ctrl + t or use a triangulate modifier.

### Sharp Edges
Again, sharp edges are self-explanatory, and you mostly won't have to deal with them. Since Jolteon is a pretty spiky model, there were some parts that had sharp edges, but you can smooth them out with the smooth tool in Sculpt or just make the edge less-sharp by moving it using G. 

## Slicing
This project was sliced in BambuStudio using an Bambu Lab A1 Mini as a build plate. Everything is contained within the jeepeonprint.3mf file, and it's all arranged with supports generated. 

<img width="609" height="362" alt="image" src="https://github.com/user-attachments/assets/56f3783d-08d5-4971-8622-3df024098146" />

All the parts that are separated must be glued together once they have been printed.

## Bill of Materials

NOTE: This BOM is only for general users. For Half Life, please refer to BOM.csv.

|Part|Quantity|Price (USD)|Vendor|Link|
|---|---|---|---|---|
|Printing (PLA)|1|$14.61|Toronto Public Library|https://tpl.ca/using-the-library/computer-services/digital-innovation-services/3d-printers/|
|Gel Super Glue|1|$0.88|Dollarama|https://dollarama.instacart.com/store/dollarama/products/27058631-adhaero-thick-gel-super-glue-3-g|
|80 & 120 Grit Sandpaper|1|$0.35|Home Depot|https://www.homedepot.ca/product/everbilt-2-95-inch-x-4-92-inch-x-1-inch-dual-grit-80-120-fine-medium-sanding-sponge/1001942562|
|Filler Primer|1|$8.88|TG Store|https://tgstore.ca/products/kq462-automotive-filler-primer?variant=51307277287717&country=CA&currency=CAD&utm_medium=product_sync&utm_source=google&utm_content=sag_organic&utm_campaign=sag_organic&srsltid=AU7gw4URmFMOGqa499MFSUJuuVvjuKM-fAgAOx2L9aUcWEAg2i1EvLpyRvo|
|Acrylic Paint|1|$3.36|Dollarama|https://dollarama.instacart.com/store/dollarama/products/27058703-artist-s-series-acrylic-paint-tubes-24-ct|
|Spray Matte Finish|1|$10.58|Walmart|http://walmart.ca/en/ip/Krylon-UV-Resistant-Clear-Coating-Matte-Clear-312-g/6000207323847|
|Taxes & Shipping|-|$8.67|-|-|
|Total|-|$46.66|-|-|

## Extra Notes
All parts for this project are either paid out of pocket or are already owned, thus no funding or grant is needed. The reason why printing is out of pocket is because I am unable to supply a cart screenshot/quote, as price may vary due to whether the print fails or not. The $14.61 is how much it is estimated to cost based on Toronto Public Library's own price per gram cost.

Additionally, the vendors labeled (Local) are local to me, so I do not have to pay for shipping as I can go to them in person. All shipping prices are based on my own address and ability to go in-person for certain vendors.

I love making art toys! It's a lot harder than I thought it would be, but I'm super glad I at least got to make one and can't wait to make more! 

