# Thinker Tinker Tech Webiste
## Author: Luke Johnson
## Info:
This webiste is developed in php using the MVC arthitecture.\
Front end uses HTML, CSS, and JavaScript.
## Template used for MVC architecture:
https://github.com/tjjoris/PHP-MVC
## Reference tutorial used in early development.:
https://youtube.com/playlist?list=PLfdtiltiRHWGXVHXX09fxXDi-DqInchFD&si=aI-J_SOajJ9d07-J
\
## Timeline: 
- ~~Week 1:~~	
	- ~~finish mvc template~~
- ~~Week 2-3:~~
	- ~~Use template for thinker tinker tech.~~
	- Convert to use Users, and Main-Page models.
	- implement basic controller logic.
	- Deploy on back end.
- Week 4-5:
	- Enable security features for user login and forum submission.
	- complete login page
- Week 6-8:
	- Additional controller logic.
	- Create front end.
- Week 9-11
	- Admin website edit controller logic and views
	- Image upload.
- Week 12-13:
	- Implement email system for contact info.

## Weeks:
- ~~Aug 9~~
- ~~Aug 16~~
- ~~Aug 23~~
- ~~Aug 30~~
- ~~Sept 6~~
- Sept 13
- Sept 20
- Sept 27
- Oct 4
- Oct 11
- Oct 18
- Oct 25
- Nov 1
- Nov 8
- Nov 15
- Nov 22
- Nov 29
- Dec 6
- Dec 13
- Dec 20
- Dec 27

## Progress notes:
3 weeks behind schedule because scope of template got expanded. \
1 additional week behind shedule due to illness. \
4 weeks behind schedule total. \
Additional time has been necessary to redesign the database structure before creating it. 

## Setup during deployment:
composer require vlucas/phpdotenv
.env goes in project root.

## Website data breakdown:
This uses the Content Block Pattern which most modern Content Management Systems use. The Class-Table Inheritance Shape, is a more relational approach which avoids nullable fields but requires more complex queries.

### Attributes used in main page table.
main_page
    - block_type
    - text
    - sort_order
    - printer_name
    - printer_price
    - printer_description
    - image
    - link

## Process for User to edit website:
- The entire webiste is composed of blocks, each one can be one the following: title, heading, subheading, paragraph, image, printer, button, or break. 
- You can add, edit, or remove a block. 
- Once a block is added a dropdown selects it's block type. 
- If it's a title, heading, subheading, paragraph, there is a text field to write the content of that block. 
- Links can be embedded in the text 
- If it's an image, a dropdown selects from available images, or a new one can be uploaded. 
- You can remove and image from available images by selecting it in the dropdown, and clicking remove image. 
- If its a button there is a text field and a link. 
- If it is a printer, there are 5 fields, printer name(text), printer price(text), printer description(text), link(url), and the image(text). the images work similar to other images. If the link is not null, a sales page button appears containing the link. 
- A break is simply a line break and has no fields. 
- For the block you are editing, there is a save, and cancel button. 
- Because this uses the Content Block Pattern, many of the fields in the database are nullable, but there is only one table, making queries much simpler. 
