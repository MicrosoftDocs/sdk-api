---
UID: NF:d2d1effectauthor.ID2D1DrawInfo.SetVertexShaderConstantBuffer
title: ID2D1DrawInfo::SetVertexShaderConstantBuffer (d2d1effectauthor.h)
description: Sets the constant buffer for this transform's vertex shader.
helpviewer_keywords: ["ID2D1DrawInfo interface [Direct2D]","SetVertexShaderConstantBuffer method","ID2D1DrawInfo.SetVertexShaderConstantBuffer","ID2D1DrawInfo::SetVertexShaderConstantBuffer","SetVertexShaderConstantBuffer","SetVertexShaderConstantBuffer method [Direct2D]","SetVertexShaderConstantBuffer method [Direct2D]","ID2D1DrawInfo interface","d2d1effectauthor/ID2D1DrawInfo::SetVertexShaderConstantBuffer","direct2d.id2d1drawinfo_setvertexshaderconstantbuffer"]
old-location: direct2d\id2d1drawinfo_setvertexshaderconstantbuffer.htm
tech.root: Direct2D
ms.assetid: 1A7991C9-BB3F-4E58-9FA7-5C4B194C33F6
ms.date: 12/05/2018
ms.keywords: ID2D1DrawInfo interface [Direct2D],SetVertexShaderConstantBuffer method, ID2D1DrawInfo.SetVertexShaderConstantBuffer, ID2D1DrawInfo::SetVertexShaderConstantBuffer, SetVertexShaderConstantBuffer, SetVertexShaderConstantBuffer method [Direct2D], SetVertexShaderConstantBuffer method [Direct2D],ID2D1DrawInfo interface, d2d1effectauthor/ID2D1DrawInfo::SetVertexShaderConstantBuffer, direct2d.id2d1drawinfo_setvertexshaderconstantbuffer
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DrawInfo::SetVertexShaderConstantBuffer
 - d2d1effectauthor/ID2D1DrawInfo::SetVertexShaderConstantBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1DrawInfo.SetVertexShaderConstantBuffer
---

# ID2D1DrawInfo::SetVertexShaderConstantBuffer


## -description

Sets the constant buffer for this transform's vertex shader.

## -parameters

### -param buffer [in]

Type: <b>const BYTE*</b>

The data applied to the constant buffer

### -param bufferCount

Type: <b>UINT32</b>

The number of bytes of data in the constant buffer.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo">ID2D1DrawInfo</a>