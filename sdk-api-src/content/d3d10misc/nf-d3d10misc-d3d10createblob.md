---
UID: NF:d3d10misc.D3D10CreateBlob
title: D3D10CreateBlob function (d3d10misc.h)
description: Create a buffer.Note  Instead of using this function, we recommend that you use the D3DCreateBlob API.
helpviewer_keywords: ["5f032879-d10b-8a54-5b40-9fa1e178b0d5","D3D10CreateBlob","D3D10CreateBlob function [Direct3D 10]","d3d10misc/D3D10CreateBlob","direct3d10.d3d10createblob"]
old-location: direct3d10\d3d10createblob.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createblob.htm
ms.date: 12/05/2018
ms.keywords: 5f032879-d10b-8a54-5b40-9fa1e178b0d5, D3D10CreateBlob, D3D10CreateBlob function [Direct3D 10], d3d10misc/D3D10CreateBlob, direct3d10.d3d10createblob
req.header: d3d10misc.h
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10CreateBlob
 - d3d10misc/D3D10CreateBlob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CreateBlob
---

# D3D10CreateBlob function


## -description

Create a buffer.
<div class="alert"><b>Note</b>  Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dcreateblob">D3DCreateBlob</a> API.</div><div> </div>

## -parameters

### -param NumBytes [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Number of bytes in the blob.

### -param ppBuffer [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">LPD3D10BLOB</a>*</b>

The address of a pointer to the buffer (see <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>