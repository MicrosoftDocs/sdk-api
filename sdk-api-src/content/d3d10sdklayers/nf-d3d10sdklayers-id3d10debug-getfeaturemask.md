---
UID: NF:d3d10sdklayers.ID3D10Debug.GetFeatureMask
title: ID3D10Debug::GetFeatureMask
author: windows-driver-content
description: Get a bitfield of flags that indicates which debug features are on or off.
old-location: direct3d10\id3d10debug_getfeaturemask.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_getfeaturemask.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 93e580f1-8c61-62ef-6cc4-d08f50c59438, GetFeatureMask, GetFeatureMask method [Direct3D 10], GetFeatureMask method [Direct3D 10],ID3D10Debug interface, ID3D10Debug interface [Direct3D 10],GetFeatureMask method, ID3D10Debug.GetFeatureMask, ID3D10Debug::GetFeatureMask, d3d10sdklayers/ID3D10Debug::GetFeatureMask, direct3d10.id3d10debug_getfeaturemask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10sdklayers.h
req.include-header: 
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10SDKLayers.h
api_name:
-	ID3D10Debug.GetFeatureMask
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Debug::GetFeatureMask


## -description


Get a bitfield of flags that indicates which debug features are on or off.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Mask of feature-mask flags bitwise ORed together. If a flag is present, then that feature will be set to on, otherwise the feature will be set to off. See <a href="https://msdn.microsoft.com/e9404531-fdf4-48e0-9ab5-f4e5b32ae077">ID3D10Debug::SetFeatureMask</a> for a list of possible feature-mask flags.




## -see-also




<a href="https://msdn.microsoft.com/2971189b-5df2-4d0a-ad7b-28dbfd6d0af3">ID3D10Debug Interface</a>
 

 

