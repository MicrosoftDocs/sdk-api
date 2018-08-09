---
UID: NF:d3dcompiler.D3DGetDebugInfo
title: D3DGetDebugInfo function
author: windows-sdk-content
description: Note  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store. Gets shader debug information.
old-location: direct3dhlsl\d3dgetdebuginfo.htm
old-project: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dgetdebuginfo.htm
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3DGetDebugInfo, D3DGetDebugInfo function [HLSL], d3dcompiler/D3DGetDebugInfo, direct3dhlsl.d3dgetdebuginfo, f21b6ffa-9910-4ce4-b2dc-07e7ad540fac
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D_BLOB_PART
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DGetDebugInfo
product: Windows
targetos: Windows
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
---

# D3DGetDebugInfo function


## -description


<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Gets shader debug information.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to source data; either uncompiled or compiled HLSL code.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pSrcData</i>.


### -param ppDebugInfo [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that contains debug information.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



Debug information is embedded in the body of the shader after calling <a href="https://msdn.microsoft.com/feb3d4d1-06ce-4141-9267-c6c771659aa7">D3DCompile</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

