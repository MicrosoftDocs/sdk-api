---
UID: NE:codecapi.eAVEncVideoColorTransferFunction
title: eAVEncVideoColorTransferFunction
author: windows-sdk-content
description: Specifies the conversion function from R'G'B' to RGB. This enumeration is used with the AVEncVideoInputColorTransferFunction and AVEncVideoOutputColorTransferFunction properties.
old-location: dshow\eavencvideocolortransferfunction.htm
old-project: DirectShow
ms.assetid: 447e6df7-6e6b-4dff-87e5-0308eb0a3dae
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: codecapi/eAVEncVideoColorTransferFunction, codecapi/eAVEncVideoColorTransferFunction_10, codecapi/eAVEncVideoColorTransferFunction_18, codecapi/eAVEncVideoColorTransferFunction_20, codecapi/eAVEncVideoColorTransferFunction_22, codecapi/eAVEncVideoColorTransferFunction_22_240M, codecapi/eAVEncVideoColorTransferFunction_22_709, codecapi/eAVEncVideoColorTransferFunction_22_8bit_sRGB, codecapi/eAVEncVideoColorTransferFunction_28, codecapi/eAVEncVideoColorTransferFunction_SameAsSource, dshow.eavencvideocolortransferfunction, eAVEncVideoColorTransferFunction, eAVEncVideoColorTransferFunction enumeration [DirectShow], eAVEncVideoColorTransferFunctionEnumeration, eAVEncVideoColorTransferFunction_10, eAVEncVideoColorTransferFunction_18, eAVEncVideoColorTransferFunction_20, eAVEncVideoColorTransferFunction_22, eAVEncVideoColorTransferFunction_22_240M, eAVEncVideoColorTransferFunction_22_709, eAVEncVideoColorTransferFunction_22_8bit_sRGB, eAVEncVideoColorTransferFunction_28, eAVEncVideoColorTransferFunction_SameAsSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoColorTransferFunction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd387884(v=VS.85).aspx">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

