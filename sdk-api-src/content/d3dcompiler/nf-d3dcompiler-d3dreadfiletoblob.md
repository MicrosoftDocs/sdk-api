---
UID: NF:d3dcompiler.D3DReadFileToBlob
title: D3DReadFileToBlob function (d3dcompiler.h)
description: Reads a file that is on disk into memory.
old-location: direct3dhlsl\d3dreadfiletoblob.htm
tech.root: direct3dhlsl
ms.assetid: 7CFB1BA6-7C36-4BDB-9705-781CCC2E7DB2
ms.date: 12/05/2018
ms.keywords: D3DReadFileToBlob, D3DReadFileToBlob function [HLSL], d3dcompiler/D3DReadFileToBlob, direct3dhlsl.d3dreadfiletoblob
ms.topic: function
f1_keywords:
- d3dcompiler/D3DReadFileToBlob
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- D3DCompiler_47.dll
api_name:
- D3DReadFileToBlob
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# D3DReadFileToBlob function


## -description


<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Reads a file  that is on disk into memory.


## -parameters




### -param pFileName [in]

A pointer to a constant null-terminated string that contains  the name of the file to read into memory.


### -param ppContents [out]

A pointer to a variable that receives a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that contains information that <b>D3DReadFileToBlob</b> read from the <i>pFileName</i> file. You can use this <b>ID3DBlob</b> interface to access the file information and pass it to other compiler functions.


## -returns



Returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.




## -remarks



<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DReadFileToBlob</b> compiler function.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>
 

 

