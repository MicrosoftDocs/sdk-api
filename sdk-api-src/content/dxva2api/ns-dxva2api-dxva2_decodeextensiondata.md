---
UID: NS:dxva2api._DXVA2_DecodeExtensionData
title: DXVA2_DecodeExtensionData (dxva2api.h)
description: Contains private data for the IDirectXVideoDecoder::Execute method.
helpviewer_keywords: ["2a1b7139-fcbb-40b0-9ed3-f9b1fe482358","DXVA2_DecodeExtensionData","DXVA2_DecodeExtensionData structure [Media Foundation]","dxva2api/DXVA2_DecodeExtensionData","mf.dxva2_decodeextensiondata"]
old-location: mf\dxva2_decodeextensiondata.htm
tech.root: mf
ms.assetid: 2a1b7139-fcbb-40b0-9ed3-f9b1fe482358
ms.date: 12/05/2018
ms.keywords: 2a1b7139-fcbb-40b0-9ed3-f9b1fe482358, DXVA2_DecodeExtensionData, DXVA2_DecodeExtensionData structure [Media Foundation], dxva2api/DXVA2_DecodeExtensionData, mf.dxva2_decodeextensiondata
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DXVA2_DecodeExtensionData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_DecodeExtensionData
 - dxva2api/_DXVA2_DecodeExtensionData
 - DXVA2_DecodeExtensionData
 - dxva2api/DXVA2_DecodeExtensionData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_DecodeExtensionData
---

# DXVA2_DecodeExtensionData structure


## -description

Contains private data for the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute">IDirectXVideoDecoder::Execute</a> method.

## -struct-fields

### -field Function

Function number. This can be zero if this argument is the default or is ignored.

### -field pPrivateInputData

Pointer to private input data passed to the driver.

### -field PrivateInputDataSize

Length of the private input data, in bytes.

### -field pPrivateOutputData

Pointer to private output data passed from the driver to the decoder.

### -field PrivateOutputDataSize

Size of the private output data, in bytes.

## -remarks

This structure corresponds to parameters of the <b>IAMVideoAccelerator::Execute</b> method in DirectX Video Acceleration (DXVA) version 1.

## -see-also

<a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams">DXVA2_DecodeExecuteParams</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>