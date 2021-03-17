---
UID: NF:d3dcommon.ID3DInclude.Close
title: ID3DInclude::Close (d3dcommon.h)
description: A user-implemented method for closing a shader
helpviewer_keywords: ["Close","Close method [Direct3D 11]","Close method [Direct3D 11]","ID3DInclude interface","ID3DInclude interface [Direct3D 11]","Close method","ID3DInclude.Close","ID3DInclude::Close","d3dcommon/ID3DInclude::Close","direct3d11.id3dinclude_close"]
old-location: direct3d11\id3dinclude_close.htm
tech.root: direct3d11
ms.assetid: d4513e15-dfe7-4919-a278-d386f25e65e5
ms.date: 12/05/2018
ms.keywords: Close, Close method [Direct3D 11], Close method [Direct3D 11],ID3DInclude interface, ID3DInclude interface [Direct3D 11],Close method, ID3DInclude.Close, ID3DInclude::Close, d3dcommon/ID3DInclude::Close, direct3d11.id3dinclude_close
req.header: d3dcommon.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3DInclude::Close
 - d3dcommon/ID3DInclude::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3DInclude.Close
---

# ID3DInclude::Close


## -description

A user-implemented method for closing a shader #include file.

## -parameters

### -param pData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

Pointer to the buffer that contains the include directives. This is the pointer that was returned by the corresponding <a href="/windows/desktop/api/d3dcommon/nf-d3dcommon-id3dinclude-open">ID3DInclude::Open</a> call.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

The user-implemented <b>Close</b> method should return S_OK. If <b>Close</b> fails when it closes the #include file, the application programming interface (API) that caused <b>Close</b> to be called fails. This failure can occur in one of the following situations:
              

<ul>
<li>The high-level shader language (HLSL) shader fails one of the <b>D3D10CompileShader***</b> functions.
              </li>
<li>The effect fails one of the <b>D3D10CreateEffect***</b> functions.
              </li>
</ul>

## -remarks

If <a href="/windows/desktop/api/d3dcommon/nf-d3dcommon-id3dinclude-open">ID3DInclude::Open</a> was successful, <b>Close</b> is guaranteed to be called before the API using the <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a> interface returns.

## -see-also

<a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3dinclude">ID3DInclude</a>



<a href="/windows/desktop/api/d3dcommon/nf-d3dcommon-id3dinclude-open">ID3DInclude::Open</a>