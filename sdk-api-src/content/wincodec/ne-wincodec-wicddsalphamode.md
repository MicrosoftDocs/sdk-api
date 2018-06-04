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

# WICDdsAlphaMode enumeration


## -description


Specifies the the meaning of pixel color component values contained in the DDS image.


## -enum-fields




### -field WICDdsAlphaModeUnknown

Alpha behavior is unspecified and must be determined by the reader.


### -field WICDdsAlphaModeStraight

The alpha data is straight.


### -field WICDdsAlphaModePremultiplied

The alpha data is premultiplied.


### -field WICDdsAlphaModeOpaque

The alpha data is opaque (UNORM value of 1). This can be used by a compliant reader as a performance optimization. For example, blending operations can be converted to copies.


### -field WICDdsAlphaModeCustom

The alpha channel contains custom data that is not alpha.


### -field WICDDSALPHAMODE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/D4EE39D6-54DC-450D-A430-2996D349BEC6">IWICDdsDecoder::GetParameters</a>



<a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>
 

 

