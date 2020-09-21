---
UID: NF:d3d11.ID3D11DeviceContext.ClearUnorderedAccessViewFloat
title: ID3D11DeviceContext::ClearUnorderedAccessViewFloat (d3d11.h)
description: Clears an unordered access resource with a float value.
helpviewer_keywords: ["2a51f18d-5ea4-ef19-5a3f-a879736bdf6a","ClearUnorderedAccessViewFloat","ClearUnorderedAccessViewFloat method [Direct3D 11]","ClearUnorderedAccessViewFloat method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","ClearUnorderedAccessViewFloat method","ID3D11DeviceContext.ClearUnorderedAccessViewFloat","ID3D11DeviceContext::ClearUnorderedAccessViewFloat","d3d11/ID3D11DeviceContext::ClearUnorderedAccessViewFloat","direct3d11.id3d11devicecontext_clearunorderedaccessviewfloat"]
old-location: direct3d11\id3d11devicecontext_clearunorderedaccessviewfloat.htm
tech.root: direct3d11
ms.assetid: c93d8638-c624-402a-8e14-c85aa7b69930
ms.date: 12/05/2018
ms.keywords: 2a51f18d-5ea4-ef19-5a3f-a879736bdf6a, ClearUnorderedAccessViewFloat, ClearUnorderedAccessViewFloat method [Direct3D 11], ClearUnorderedAccessViewFloat method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],ClearUnorderedAccessViewFloat method, ID3D11DeviceContext.ClearUnorderedAccessViewFloat, ID3D11DeviceContext::ClearUnorderedAccessViewFloat, d3d11/ID3D11DeviceContext::ClearUnorderedAccessViewFloat, direct3d11.id3d11devicecontext_clearunorderedaccessviewfloat
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
 - ID3D11DeviceContext::ClearUnorderedAccessViewFloat
 - d3d11/ID3D11DeviceContext::ClearUnorderedAccessViewFloat
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
 - ID3D11DeviceContext.ClearUnorderedAccessViewFloat
---

# ID3D11DeviceContext::ClearUnorderedAccessViewFloat


## -description

Clears an <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources">unordered access</a> resource with a float value.

## -parameters

### -param pUnorderedAccessView [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

The <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> to clear.

### -param Values [in]

Type: <b>const FLOAT[4]</b>

Values to copy to corresponding channels, see remarks.

## -remarks

This API works on FLOAT, UNORM, and SNORM unordered access views (UAVs), with format conversion from FLOAT to *NORM where appropriate. On other UAVs, the operation is invalid and the call will not reach the driver.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>