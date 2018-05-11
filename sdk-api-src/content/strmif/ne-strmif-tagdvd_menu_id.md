---
UID: NE:strmif.tagDVD_MENU_ID
title: tagDVD_MENU_ID
author: windows-driver-content
description: Specifies the DVD menu in a call to IDvdControl2::ShowMenu.
old-location: dshow\dvd_menu_id.htm
old-project: DirectShow
ms.assetid: 2fd107d7-7531-4bce-89b9-b44388b47b91
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DVD_MENU_Angle, DVD_MENU_Audio, DVD_MENU_Chapter, DVD_MENU_ID, DVD_MENU_ID , DVD_MENU_ID enumeration [DirectShow], DVD_MENU_IDEnumeration, DVD_MENU_Root, DVD_MENU_Subpicture, DVD_MENU_Title, dshow.dvd_menu_id, strmif/DVD_MENU_Angle, strmif/DVD_MENU_Audio, strmif/DVD_MENU_Chapter, strmif/DVD_MENU_ID, strmif/DVD_MENU_Root, strmif/DVD_MENU_Subpicture, strmif/DVD_MENU_Title, tagDVD_MENU_ID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.typenames: DVD_MENU_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	DVD_MENU_ID
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 6.01
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
 

 

