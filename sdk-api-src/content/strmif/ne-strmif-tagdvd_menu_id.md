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

# tagDVD_MENU_ID enumeration


## -description



Specifies the DVD menu in a call to <a href="https://msdn.microsoft.com/7427ff6c-875b-40ce-aa96-3d32b607dc56">IDvdControl2::ShowMenu</a>.




## -enum-fields




### -field DVD_MENU_Title

Specifies the top menu in a DVD-Video volume. This menu is also known as the Title Menu or Video Manager Menu and it provides access to all VTS (Video Title Set) menus on the disc.


### -field DVD_MENU_Root

Specifies the root menu for a VTS.


### -field DVD_MENU_Subpicture

Specifies the subpicture submenu in a VTS menu.


### -field DVD_MENU_Audio

Specifies the audio submenu in a VTS menu.


### -field DVD_MENU_Angle

Specifies the angle submenu in a VTS menu.


### -field DVD_MENU_Chapter

Choose a chapter submenu in a VTS menu.


## -remarks



The root menu always provides a means of getting to the subpicture, audio, angle and chapter menus if they exist.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/7427ff6c-875b-40ce-aa96-3d32b607dc56">IDvdControl2::ShowMenu</a>
 

 

