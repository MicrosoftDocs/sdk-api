---
UID: NS:strmif.tagDVD_MenuAttributes
title: tagDVD_MenuAttributes
author: windows-sdk-content
description: The DVD_MenuAttributes structure contains information about a DVD menu. The IDvdInfo2::GetTitleAttributes method fills in a DVD_MenuAttributes structure for a specified stream.
old-location: dshow\dvd_menuattributes.htm
tech.root: DirectShow
ms.assetid: 074593e2-f4f4-44d3-a37c-209b4e798a52
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DVD_MenuAttributes, DVD_MenuAttributes structure [DirectShow], DVD_MenuAttributesStructure, dshow.dvd_menuattributes, strmif/DVD_MenuAttributes, tagDVD_MenuAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_MenuAttributes
product: Windows
targetos: Windows
req.typenames: DVD_MenuAttributes
req.redist: 
---

# tagDVD_MenuAttributes structure


## -description



The <b>DVD_MenuAttributes</b> structure contains information about a DVD menu. The <a href="https://msdn.microsoft.com/4e901e14-9e98-4ca5-ae37-7a4564b187ab">IDvdInfo2::GetTitleAttributes</a> method fills in a DVD_MenuAttributes structure for a specified stream.




## -struct-fields




### -field fCompatibleRegion

An array of <b>TRUE</b>/<b>FALSE</b> values indicating with which DVD regions the disc's authored region is compatible. The eight array indexes (numbered 0-7) correspond to the eight DVD regions (numbered 1-8). This array is only filled in when the menu being queried is the Video Manager Menu (the main menu for the entire disc).

<div class="alert"><b>Important</b>  A value of 0 (<b>FALSE</b>) indicates that the region is compatible (permitted). A value of 1 (<b>TRUE</b>) indicates that the region is not compatible. This member should have been named <i>fIncompatibleRegion</i>.</div>
<div> </div>

### -field VideoAttributes

A <a href="https://msdn.microsoft.com/b395a322-d63e-41a0-b97a-88f99aeba0e5">DVD_VideoAttributes</a> structure containing the video attributes of the menu. This applies to both a VMGM and VTSM.


### -field fAudioPresent

A variable of type BOOL indicating whether the menu has an audio stream.


### -field AudioAttributes

A <a href="https://msdn.microsoft.com/a4365c05-718e-4d48-bb2c-a13a609df82f">DVD_AudioAttributes</a> structure containing information about the menu's audio stream. This structure will only be filled in if <i>fAudioPresent</i> is <b>TRUE</b>.


### -field fSubpicturePresent

A variable of type BOOL indicating whether the menu has a subpicture stream.


### -field SubpictureAttributes

A <a href="https://msdn.microsoft.com/55ddfa21-5600-4aa9-b554-7ff7f3c05b91">DVD_SubpictureAttributes</a> structure containing information about the menu's subpicture stream. This structure will only be filled in if <i>fSubpicturePresent</i> is <b>TRUE</b>.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

