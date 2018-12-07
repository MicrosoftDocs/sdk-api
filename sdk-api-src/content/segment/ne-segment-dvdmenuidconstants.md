---
UID: NE:segment.DVDMenuIDConstants
title: DVDMenuIDConstants
author: windows-sdk-content
description: The DVDMenuID constants define menu type ID numbers used to display specific menus.
old-location: mstv\dvdmenuid_constants.htm
tech.root: mstv
ms.assetid: f58ce7b6-6fc4-4766-bf8a-180a5568d27c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DVDMenuID Constants, DVDMenuIDConstants, DVDMenuIDConstants enumeration [Microsoft TV Technologies], DVDMenuIDConstantsEnumeration, dvdMenu_Angle, dvdMenu_Audio, dvdMenu_Chapter, dvdMenu_Root, dvdMenu_Subpicture, dvdMenu_Title, enumeration [Microsoft TV Technologies], mstv.dvdmenuid_constants, segment/, segment/dvdMenu_Angle, segment/dvdMenu_Audio, segment/dvdMenu_Chapter, segment/dvdMenu_Root, segment/dvdMenu_Subpicture, segment/dvdMenu_Title
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: segment.h
req.include-header: Msvidctl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Segment.h
api_name:
 - DVDMenuIDConstants
product: Windows
targetos: Windows
req.typenames: DVDMenuIDConstants
req.redist: 
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




<a href="https://msdn.microsoft.com/library/Dd695183(v=VS.85).aspx">MSVidWebDVD Constants</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376389(v=VS.85).aspx">ShowMenu</a>
 

 

