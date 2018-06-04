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

# tagDVD_VideoAttributes structure


## -description



The <code>DVD_VideoAttributes</code> structure describes the attributes of the video stream for the current title or menu.




## -struct-fields




### -field fPanscanPermitted

<b>TRUE</b> means the picture can be shown as pan-scan if the display aspect ratio is 4 x 3.


### -field fLetterboxPermitted

<b>TRUE</b> means the picture can be shown as letterbox if the display aspect ratio is 4 x 3.


### -field ulAspectX

The video stream's X aspect (4 or 16).


### -field ulAspectY

The video stream's Y aspect (3 or 9).


### -field ulFrameRate

The frame rate in hertz (Hz), either 50 or 60.


### -field ulFrameHeight

The frame height in lines (525 for a frame rate of 60 Hz or 625 for 50 Hz).


### -field Compression

Variable of type <a href="https://msdn.microsoft.com/e147a860-4c69-4da0-96d1-dfc4957880d9">DVD_VIDEO_COMPRESSION</a> indicating the MPEG compression type used on the disc.


### -field fLine21Field1InGOP

<b>TRUE</b> means there is user data in line 21, field 1.


### -field fLine21Field2InGOP

<b>TRUE</b> means there is user data in line 21, field 2.


### -field ulSourceResolutionX

The x-axis source resolution (352, 704, or 720).


### -field ulSourceResolutionY

The y-axis source resolution (240, 480, 288, or 576).


### -field fIsSourceLetterboxed

<b>TRUE</b> means the source video is in letterbox format. Subpictures and menu buttons can only be displayed in the active video area.


### -field fIsFilmMode

For 625/50 Hz systems, <b>TRUE</b> means "film mode" and <b>FALSE</b> means "camera mode."


## -remarks



This structure is filled when an application calls the <a href="https://msdn.microsoft.com/92bd3af9-7057-4bf7-9026-d4862c271a03">IDvdInfo2::GetCurrentVideoAttributes</a> method.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

