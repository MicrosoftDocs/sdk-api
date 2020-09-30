---
UID: NF:d3dcompiler.D3DWriteBlobToFile
title: D3DWriteBlobToFile function (d3dcompiler.h)
description: Writes a memory blob to a file on disk.
helpviewer_keywords: ["D3DWriteBlobToFile","D3DWriteBlobToFile function [HLSL]","d3dcompiler/D3DWriteBlobToFile","direct3dhlsl.d3dwriteblobtofile"]
old-location: direct3dhlsl\d3dwriteblobtofile.htm
tech.root: direct3dhlsl
ms.assetid: F21FF3B4-5F69-4C93-9F93-6A12324A664A
ms.date: 12/05/2018
ms.keywords: D3DWriteBlobToFile, D3DWriteBlobToFile function [HLSL], d3dcompiler/D3DWriteBlobToFile, direct3dhlsl.d3dwriteblobtofile
req.header: d3dcompiler.h
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
 - D3DWriteBlobToFile
 - d3dcompiler/D3DWriteBlobToFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DWriteBlobToFile
---

# D3DWriteBlobToFile function


## -description

<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Writes a memory blob to a file on disk.

## -parameters

### -param pBlob [in]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>*</b>

A pointer to a <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that contains the memory blob to write to the file that the <i>pFileName</i> parameter specifies.

### -param pFileName [in]

Type: <b>LPCWSTR</b>

A pointer to a constant null-terminated string that contains  the name of the file to which to write.

### -param bOverwrite [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A Boolean value that specifies whether to overwrite information in the <i>pFileName</i> file. TRUE specifies to overwrite information and FALSE specifies not to overwrite information.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DWriteBlobToFile</b> compiler function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>