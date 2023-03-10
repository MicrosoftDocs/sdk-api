---
UID: NS:d3d11.D3D11_VIDEO_DECODER_EXTENSION
title: D3D11_VIDEO_DECODER_EXTENSION (d3d11.h)
description: Contains driver-specific data for the ID3D11VideoContext::DecoderExtension method.
helpviewer_keywords: ["D3D11_VIDEO_DECODER_EXTENSION","D3D11_VIDEO_DECODER_EXTENSION structure [Media Foundation]","d3d11/D3D11_VIDEO_DECODER_EXTENSION","mf.d3d11_video_decoder_extension"]
old-location: mf\d3d11_video_decoder_extension.htm
tech.root: mf
ms.assetid: F82746A4-16AB-49B5-96C8-777675416467
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_DECODER_EXTENSION, D3D11_VIDEO_DECODER_EXTENSION structure [Media Foundation], d3d11/D3D11_VIDEO_DECODER_EXTENSION, mf.d3d11_video_decoder_extension
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: D3D11_VIDEO_DECODER_EXTENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_DECODER_EXTENSION
 - d3d11/D3D11_VIDEO_DECODER_EXTENSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_EXTENSION
---

# D3D11_VIDEO_DECODER_EXTENSION structure


## -description

Contains driver-specific data for the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderextension">ID3D11VideoContext::DecoderExtension</a> method.

## -struct-fields

### -field Function

The function number. This number identifies the operation to perform. Currently no function numbers are defined.

### -field pPrivateInputData

A pointer to a buffer that contains input data for the driver.

### -field PrivateInputDataSize

The size of the <b>pPrivateInputData</b> buffer, in bytes.

### -field pPrivateOutputData

A pointer to a buffer that the driver can use to write output data.

### -field PrivateOutputDataSize

The size of the <b>pPrivateOutputData</b> buffer, in bytes.

### -field ResourceCount

The number of elements in the <b>ppResourceList</b> array. If <b>ppResourceList</b> is <b>NULL</b>, set <b>ResourceCount</b> to zero.

### -field ppResourceList

The address of an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> pointers. Use this member to pass Direct3D resources to the driver.

## -remarks

The exact meaning of each structure member depends on the value of <b>Function</b>.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>