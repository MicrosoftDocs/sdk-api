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

# ID3D11VideoContext1::VideoProcessorGetStreamMirror


## -description


Gets values that indicate whether the video processor input stream is  being flipped vertically or horizontally.


## -parameters




### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param StreamIndex [in]

Type: <b>UINT</b>

An index identifying the input stream.


### -param pEnable [out]

Type: <b>BOOL*</b>

A pointer to a boolean value indicating whether mirroring is enabled. True if mirroring is enabled; otherwise, false.


### -param pFlipHorizontal [out]

Type: <b>BOOL*</b>

A pointer to a boolean value indicating whether the stream is being flipped horizontally. True if the stream is being flipped horizontally; otherwise, false.


### -param pFlipVertical [out]

Type: <b>BOOL*</b>

A pointer to a boolean value indicating whether the stream is being flipped vertically. True if the stream is being flipped vertically; otherwise, false.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

