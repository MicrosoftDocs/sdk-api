---
UID: NS:dxva2api._DXVA2_DecodeExecuteParams
title: DXVA2_DecodeExecuteParams (dxva2api.h)
description: Contains parameters for the IDirectXVideoDecoder::Execute method.
helpviewer_keywords: ["DXVA2_DecodeExecuteParams","DXVA2_DecodeExecuteParams structure [Media Foundation]","dxva2api/DXVA2_DecodeExecuteParams","e0e95e9b-6d53-4b90-a933-243023dc31ef","mf.dxva2_decodeexecuteparams"]
old-location: mf\dxva2_decodeexecuteparams.htm
tech.root: mf
ms.assetid: e0e95e9b-6d53-4b90-a933-243023dc31ef
ms.date: 12/05/2018
ms.keywords: DXVA2_DecodeExecuteParams, DXVA2_DecodeExecuteParams structure [Media Foundation], dxva2api/DXVA2_DecodeExecuteParams, e0e95e9b-6d53-4b90-a933-243023dc31ef, mf.dxva2_decodeexecuteparams
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
req.typenames: DXVA2_DecodeExecuteParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_DecodeExecuteParams
 - dxva2api/_DXVA2_DecodeExecuteParams
 - DXVA2_DecodeExecuteParams
 - dxva2api/DXVA2_DecodeExecuteParams
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
 - DXVA2_DecodeExecuteParams
---

# DXVA2_DecodeExecuteParams structure


## -description

Contains parameters for the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute">IDirectXVideoDecoder::Execute</a> method.

## -struct-fields

### -field NumCompBuffers

Number of compressed buffers.

### -field pCompressedBuffers

Pointer to an array of <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc">DXVA2_DecodeBufferDesc</a> structures that describe the compressed buffers. The number of elements in the array is given by the <b>NumCompBuffers</b> member.

### -field pExtensionData

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata">DXVA2_DecodeExtensionData</a> structure that contains private data. Set this member to <b>NULL</b> unless you need to send private data to or from the driver.

## -see-also

<a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc">DXVA2_DecodeBufferDesc</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>