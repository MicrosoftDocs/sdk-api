---
UID: NF:d3d11.ID3D11DeviceContext.SOGetTargets
title: ID3D11DeviceContext::SOGetTargets (d3d11.h)
description: Get the target output buffers for the stream-output stage of the pipeline.
helpviewer_keywords: ["90e06f28-a9a0-3b66-9901-3e60886b896d","ID3D11DeviceContext interface [Direct3D 11]","SOGetTargets method","ID3D11DeviceContext.SOGetTargets","ID3D11DeviceContext::SOGetTargets","SOGetTargets","SOGetTargets method [Direct3D 11]","SOGetTargets method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::SOGetTargets","direct3d11.id3d11devicecontext_sogettargets"]
old-location: direct3d11\id3d11devicecontext_sogettargets.htm
tech.root: direct3d11
ms.assetid: 878402ed-0c89-42db-8210-d9a90b347226
ms.date: 12/05/2018
ms.keywords: 90e06f28-a9a0-3b66-9901-3e60886b896d, ID3D11DeviceContext interface [Direct3D 11],SOGetTargets method, ID3D11DeviceContext.SOGetTargets, ID3D11DeviceContext::SOGetTargets, SOGetTargets, SOGetTargets method [Direct3D 11], SOGetTargets method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::SOGetTargets, direct3d11.id3d11devicecontext_sogettargets
req.header: d3d11.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::SOGetTargets
 - d3d11/ID3D11DeviceContext::SOGetTargets
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.SOGetTargets
---

# ID3D11DeviceContext::SOGetTargets


## -description

Get the target output buffers for the stream-output stage of the pipeline.

## -parameters

### -param NumBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers to get.

### -param ppSOTargets [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>**</b>

An array of output buffers (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>) to be retrieved from the device.

## -remarks

A maximum of four output buffers can be retrieved.

The offsets to the output buffers pointed to in the returned <i>ppSOTargets</i> array may be assumed to be -1 (append), as defined for use in <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-sosettargets">ID3D11DeviceContext::SOSetTargets</a>.
        

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>