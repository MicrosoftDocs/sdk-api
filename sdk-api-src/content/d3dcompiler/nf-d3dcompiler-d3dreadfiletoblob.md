---
UID: NF:d3dcompiler.D3DReadFileToBlob
title: D3DReadFileToBlob function
author: windows-sdk-content
description: Reads a file that is on disk into memory.
old-location: direct3dhlsl\d3dreadfiletoblob.htm
tech.root: direct3dhlsl
ms.assetid: 7CFB1BA6-7C36-4BDB-9705-781CCC2E7DB2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: D3DReadFileToBlob, D3DReadFileToBlob function [HLSL], d3dcompiler/D3DReadFileToBlob, direct3dhlsl.d3dreadfiletoblob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3DReadFileToBlob function


## -description


<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Reads a file  that is on disk into memory.


## -parameters




### -param pFileName [in]

A pointer to a constant null-terminated string that contains  the name of the file to read into memory.


### -param ppContents [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that contains information that <b>D3DReadFileToBlob</b> read from the <i>pFileName</i> file. You can use this <b>ID3DBlob</b> interface to access the file information and pass it to other compiler functions.


## -returns



Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DReadFileToBlob</b> compiler function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aacc5207-3ec8-4031-b5c9-f7c0fb7b7095">Functions</a>
 

 

