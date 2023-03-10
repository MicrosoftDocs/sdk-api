---
UID: NF:d3d10sdklayers.ID3D10Debug.GetFeatureMask
title: ID3D10Debug::GetFeatureMask (d3d10sdklayers.h)
description: Get a bitfield of flags that indicates which debug features are on or off. (ID3D10Debug.GetFeatureMask)
helpviewer_keywords: ["93e580f1-8c61-62ef-6cc4-d08f50c59438","GetFeatureMask","GetFeatureMask method [Direct3D 10]","GetFeatureMask method [Direct3D 10]","ID3D10Debug interface","ID3D10Debug interface [Direct3D 10]","GetFeatureMask method","ID3D10Debug.GetFeatureMask","ID3D10Debug::GetFeatureMask","d3d10sdklayers/ID3D10Debug::GetFeatureMask","direct3d10.id3d10debug_getfeaturemask"]
old-location: direct3d10\id3d10debug_getfeaturemask.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_getfeaturemask.htm
ms.date: 12/05/2018
ms.keywords: 93e580f1-8c61-62ef-6cc4-d08f50c59438, GetFeatureMask, GetFeatureMask method [Direct3D 10], GetFeatureMask method [Direct3D 10],ID3D10Debug interface, ID3D10Debug interface [Direct3D 10],GetFeatureMask method, ID3D10Debug.GetFeatureMask, ID3D10Debug::GetFeatureMask, d3d10sdklayers/ID3D10Debug::GetFeatureMask, direct3d10.id3d10debug_getfeaturemask
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Debug::GetFeatureMask
 - d3d10sdklayers/ID3D10Debug::GetFeatureMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10Debug.GetFeatureMask
---

# ID3D10Debug::GetFeatureMask


## -description

Get a bitfield of flags that indicates which debug features are on or off.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Mask of feature-mask flags bitwise ORed together. If a flag is present, then that feature will be set to on, otherwise the feature will be set to off. See <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask">ID3D10Debug::SetFeatureMask</a> for a list of possible feature-mask flags.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10debug">ID3D10Debug Interface</a>
