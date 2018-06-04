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

# tagIMAGEINFO structure


## -description


Contains information about an image in an image list. This structure is used with the <a href="https://msdn.microsoft.com/a08fbc4d-96f0-403d-8062-0592ab32dc5c">IImageList::GetImageInfo</a> function. 


## -struct-fields




### -field hbmImage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to the bitmap that contains the images. 


### -field hbmMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to a monochrome bitmap that contains the masks for the images. If the image list does not contain a mask, this member is <b>NULL</b>. 


### -field Unused1

Type: <b>int</b>

Not used. This member should always be zero. 


### -field Unused2

Type: <b>int</b>

Not used. This member should always be zero. 


### -field rcImage

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The bounding rectangle of the specified image within the bitmap specified by 
					<b>hbmImage</b>. 

