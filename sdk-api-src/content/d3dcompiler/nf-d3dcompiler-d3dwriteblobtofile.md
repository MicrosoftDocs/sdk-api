---
UID: NF:d3dcompiler.D3DWriteBlobToFile
title: D3DWriteBlobToFile function (d3dcompiler.h)
author: windows-sdk-content
description: Writes a memory blob to a file on disk.
old-location: direct3dhlsl\d3dwriteblobtofile.htm
tech.root: direct3dhlsl
ms.assetid: F21FF3B4-5F69-4C93-9F93-6A12324A664A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3DWriteBlobToFile, D3DWriteBlobToFile function [HLSL], d3dcompiler/D3DWriteBlobToFile, direct3dhlsl.d3dwriteblobtofile
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
 - D3DWriteBlobToFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3DWriteBlobToFile function


## -description


<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Writes a memory blob to a file on disk.


## -parameters




### -param pBlob [in]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that contains the memory blob to write to the file that the <i>pFileName</i> parameter specifies.


### -param pFileName [in]

Type: <b>LPCWSTR</b>

A pointer to a constant null-terminated string that contains  the name of the file to which to write.


### -param bOverwrite [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A Boolean value that specifies whether to overwrite information in the <i>pFileName</i> file. TRUE specifies to overwrite information and FALSE specifies not to overwrite information.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DWriteBlobToFile</b> compiler function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd607342(v=VS.85).aspx">Functions</a>
 

 

