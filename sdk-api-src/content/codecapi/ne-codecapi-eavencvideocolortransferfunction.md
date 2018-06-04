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

# eAVEncVideoColorTransferFunction enumeration


## -description



Specifies the conversion function from R'G'B' to RGB. This enumeration is used with the <a href="https://msdn.microsoft.com/ccfdeb65-6188-4fea-bbef-2510271fbf1e">AVEncVideoInputColorTransferFunction</a> and <a href="https://msdn.microsoft.com/89efb1c7-cf77-465c-b6b3-5f89773c524b">AVEncVideoOutputColorTransferFunction</a> properties.




## -enum-fields




### -field eAVEncVideoColorTransferFunction_SameAsSource

Use the same function as the input video. This flag applies to the <b>AVEncVideoOutputColorTransferFunction</b> property only.


### -field eAVEncVideoColorTransferFunction_10

Linear RGB (gamma = 1.0).


### -field eAVEncVideoColorTransferFunction_18

True 1.8 gamma. L' = L^1/1.8.


### -field eAVEncVideoColorTransferFunction_20

True 2.0 gamma. L' = L^1/2.0..


### -field eAVEncVideoColorTransferFunction_22

True 2.2 gamma. L' = L^1/2.2..


### -field eAVEncVideoColorTransferFunction_22_709

Gamma 2.2 curve with a linear segment in the lower range. L' = 4.5L, for L &lt; 0.018; L' = 1.099L^0.45.- 0.099, for L &gt;= 0.018. This transfer function is used in BT-709, SMPTE 296M, SMPTE 170M, BT-470, and SPMTE 274M.


### -field eAVEncVideoColorTransferFunction_22_240M

Gamma 2.2 curve with a linear segment in the lower range. L' = 4.0L, for L &lt; 0.0228; L' = 1.1115^L0.45.- 0.01115, for L &gt;= 0.0228. This transfer function is used in SPMTE 240M.


### -field eAVEncVideoColorTransferFunction_22_8bit_sRGB

Gamma 2.4 curve with a linear segment in the lower range. L' = L/12.92, for L &lt; 0.03928; L' = ((L + 0.055) / 1.055)^2.4., for L &gt;= 0.03928.


### -field eAVEncVideoColorTransferFunction_28

True 2.8 gamma. L' = L^1/2.8..


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

