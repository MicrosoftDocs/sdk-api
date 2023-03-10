---
UID: NF:d2d1effectauthor.ID2D1ComputeInfo.SetComputeShaderConstantBuffer
title: ID2D1ComputeInfo::SetComputeShaderConstantBuffer (d2d1effectauthor.h)
description: Establishes or changes the constant buffer data for this transform.
helpviewer_keywords: ["ID2D1ComputeInfo interface [Direct2D]","SetComputeShaderConstantBuffer method","ID2D1ComputeInfo.SetComputeShaderConstantBuffer","ID2D1ComputeInfo::SetComputeShaderConstantBuffer","SetComputeShaderConstantBuffer","SetComputeShaderConstantBuffer method [Direct2D]","SetComputeShaderConstantBuffer method [Direct2D]","ID2D1ComputeInfo interface","d2d1effectauthor/ID2D1ComputeInfo::SetComputeShaderConstantBuffer","direct2d.id2d1computeinfo_setcomputeshaderconstantbuffer"]
old-location: direct2d\id2d1computeinfo_setcomputeshaderconstantbuffer.htm
tech.root: Direct2D
ms.assetid: E7443E72-F8F6-48C4-A9BD-5EF132E8C090
ms.date: 12/05/2018
ms.keywords: ID2D1ComputeInfo interface [Direct2D],SetComputeShaderConstantBuffer method, ID2D1ComputeInfo.SetComputeShaderConstantBuffer, ID2D1ComputeInfo::SetComputeShaderConstantBuffer, SetComputeShaderConstantBuffer, SetComputeShaderConstantBuffer method [Direct2D], SetComputeShaderConstantBuffer method [Direct2D],ID2D1ComputeInfo interface, d2d1effectauthor/ID2D1ComputeInfo::SetComputeShaderConstantBuffer, direct2d.id2d1computeinfo_setcomputeshaderconstantbuffer
req.header: d2d1effectauthor.h
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
 - ID2D1ComputeInfo::SetComputeShaderConstantBuffer
 - d2d1effectauthor/ID2D1ComputeInfo::SetComputeShaderConstantBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1effectauthor.h
api_name:
 - ID2D1ComputeInfo.SetComputeShaderConstantBuffer
---

# ID2D1ComputeInfo::SetComputeShaderConstantBuffer


## -description

Establishes or changes the constant buffer data for this transform.

## -parameters

### -param buffer [in]

Type: <b>const BYTE*</b>

The data applied to the constant buffer.

### -param bufferCount

Type: <b>UINT32</b>

The number of bytes of data in the constant buffer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo">ID2D1ComputeInfo</a>