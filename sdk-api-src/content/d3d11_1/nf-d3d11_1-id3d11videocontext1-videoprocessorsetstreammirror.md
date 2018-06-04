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

# ID3D11VideoContext1::VideoProcessorSetStreamMirror


## -description


Specifies whether the video processor input stream should be flipped vertically or horizontally.


## -parameters




### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param StreamIndex [in]

Type: <b>UINT</b>

An index identifying the input stream.


### -param Enable [in]

Type: <b>BOOL</b>

True if mirroring should be enabled; otherwise, false.


### -param FlipHorizontal [in]

Type: <b>BOOL</b>

True if the stream should be flipped horizontally; otherwise, false.


### -param FlipVertical [in]

Type: <b>BOOL</b>

True if the stream should be flipped vertically; otherwise, false.


## -returns



This method does not return a value.




## -remarks



When used in combination, transformations on the processor input stream should be applied in the following order:

<ul>
<li>Rotation</li>
<li>Mirroring</li>
<li>Source clipping</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

