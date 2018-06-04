---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DVDMenuIDConstants enumeration


## -description


The <b>DVDMenuID</b> constants define menu type ID numbers used to display specific menus.


## -enum-fields




### -field dvdMenu_Title

Title menu, also called the Video Manager Menu.




### -field dvdMenu_Root

Root menu, the menu for one video title set, which can contain one title or a group of titles.




### -field dvdMenu_Subpicture

Subpicture menu.




### -field dvdMenu_Audio

Audio menu.


### -field dvdMenu_Angle

Angle menu.


### -field dvdMenu_Chapter

Chapter menu.


## -remarks



All the titles in a title set share the same Subpicture, Audio, Angle, and Chapter menus.




## -see-also




<a href="mstv.msvidwebdvd_constants">MSVidWebDVD Constants</a>



<a href="mstv.msvidwebdvd_showmenu_method">ShowMenu</a>
 

 

