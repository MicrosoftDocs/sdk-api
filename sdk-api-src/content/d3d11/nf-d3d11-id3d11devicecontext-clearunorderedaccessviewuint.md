---
UID: NF:d3d11.ID3D11DeviceContext.ClearUnorderedAccessViewUint
title: ID3D11DeviceContext::ClearUnorderedAccessViewUint (d3d11.h)
description: Clears an unordered access resource with bit-precise values.
helpviewer_keywords: ["6de62b79-ec47-d4cc-7834-5acc4c87fa8d","ClearUnorderedAccessViewUint","ClearUnorderedAccessViewUint method [Direct3D 11]","ClearUnorderedAccessViewUint method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","ClearUnorderedAccessViewUint method","ID3D11DeviceContext.ClearUnorderedAccessViewUint","ID3D11DeviceContext::ClearUnorderedAccessViewUint","d3d11/ID3D11DeviceContext::ClearUnorderedAccessViewUint","direct3d11.id3d11devicecontext_clearunorderedaccessviewuint"]
old-location: direct3d11\id3d11devicecontext_clearunorderedaccessviewuint.htm
tech.root: direct3d11
ms.assetid: 73e70330-63cb-4ba6-b6e5-fc9707fb9f31
ms.date: 12/05/2018
ms.keywords: 6de62b79-ec47-d4cc-7834-5acc4c87fa8d, ClearUnorderedAccessViewUint, ClearUnorderedAccessViewUint method [Direct3D 11], ClearUnorderedAccessViewUint method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],ClearUnorderedAccessViewUint method, ID3D11DeviceContext.ClearUnorderedAccessViewUint, ID3D11DeviceContext::ClearUnorderedAccessViewUint, d3d11/ID3D11DeviceContext::ClearUnorderedAccessViewUint, direct3d11.id3d11devicecontext_clearunorderedaccessviewuint
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
 - ID3D11DeviceContext::ClearUnorderedAccessViewUint
 - d3d11/ID3D11DeviceContext::ClearUnorderedAccessViewUint
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
 - ID3D11DeviceContext.ClearUnorderedAccessViewUint
---

# ID3D11DeviceContext::ClearUnorderedAccessViewUint


## -description

Clears an <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources">unordered access</a> resource with bit-precise values.

## -parameters

### -param pUnorderedAccessView [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

The <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> to clear.

### -param Values [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>[4]</b>

Values to copy to corresponding channels, see remarks.

## -remarks

This API copies the lower n<sub>i</sub> bits from each array element i to the corresponding channel, where n<sub>i</sub> is the number of bits in 
      the ith channel of the resource format (for example, R8G8B8_FLOAT has 8 bits for the first 3 channels). This works on any UAV with no format conversion. 
      For a raw or structured buffer view, only the first array element value is used.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>