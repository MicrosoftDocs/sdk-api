---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE
tech.root: mf
title: D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE
ms.date: 07/01/2021
targetos: Windows
description: Represents the reconstructed picture generated from the input frame passed to the encode operation.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE
f1_keywords:
 - D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE
 - d3d12video/D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE
dev_langs:
 - c++
---

## -description

Represents the reconstructed picture generated from the input frame passed to the encode operation.

## -struct-fields

### -field pReconstructedPicture

A [ID3D12Resource](../d3d12/nn-d3d12-id3d12resource) representing the reconstructed picture generated from the input frame.
 
### -field ReconstructedPictureSubresource

A UINT64 specifying the subresource index for *pReconstructedPicture*.

## -remarks

## -see-also

