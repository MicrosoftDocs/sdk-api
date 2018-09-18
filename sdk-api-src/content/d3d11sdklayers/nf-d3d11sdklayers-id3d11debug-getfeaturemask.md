---
UID: NF:d3d11sdklayers.ID3D11Debug.GetFeatureMask
title: ID3D11Debug::GetFeatureMask
author: windows-sdk-content
description: Get a bitfield of flags that indicates which debug features are on or off.
old-location: direct3d11\id3d11debug_getfeaturemask.htm
tech.root: direct3d11
ms.assetid: 5c70c85a-77a5-4e3b-9247-7686d43cbd1a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 433c837f-7fd5-8e03-76ca-d912879e10fd, GetFeatureMask, GetFeatureMask method [Direct3D 11], GetFeatureMask method [Direct3D 11],ID3D11Debug interface, ID3D11Debug interface [Direct3D 11],GetFeatureMask method, ID3D11Debug.GetFeatureMask, ID3D11Debug::GetFeatureMask, d3d11sdklayers/ID3D11Debug::GetFeatureMask, direct3d11.id3d11debug_getfeaturemask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Debug.GetFeatureMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Debug::GetFeatureMask


## -description


Get a bitfield of flags that indicates which debug features are on or off.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Mask of feature-mask flags bitwise ORed together. If a flag is present, then that feature will be set to on, otherwise the feature will be set to off. See <a href="https://msdn.microsoft.com/60f9da61-dc97-4b6d-b187-df3605ad9336">ID3D11Debug::SetFeatureMask</a> for a list of possible feature-mask flags.




## -see-also




<a href="https://msdn.microsoft.com/2c640295-7a91-4a7a-92d3-909d288eb0d6">ID3D11Debug Interface</a>
 

 

