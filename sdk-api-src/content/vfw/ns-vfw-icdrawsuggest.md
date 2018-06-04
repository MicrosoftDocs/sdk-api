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

# ICDRAWSUGGEST structure


## -description



The <b>ICDRAWSUGGEST</b> structure contains compression parameters used with the <a href="https://msdn.microsoft.com/e3e97790-dbd1-4436-9830-5218ae1f949b">ICM_DRAW_SUGGESTFORMAT</a> message to suggest an appropriate input format.




## -struct-fields




### -field lpbiIn

Pointer to the structure containing the compressed input format.


### -field lpbiSuggest

Pointer to a buffer to return a compatible input format for the renderer.


### -field dxSrc

Width of the source rectangle.


### -field dySrc

Height of the source rectangle.


### -field dxDst

Width of the destination rectangle.


### -field dyDst

Height of the destination rectangle.


### -field hicDecompressor

Handle to a decompressor that supports the format of data described in <b>lpbiIn</b>.


## -see-also




<a href="https://msdn.microsoft.com/e3e97790-dbd1-4436-9830-5218ae1f949b">ICM_DRAW_SUGGESTFORMAT</a>



Video Compression Manager



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

