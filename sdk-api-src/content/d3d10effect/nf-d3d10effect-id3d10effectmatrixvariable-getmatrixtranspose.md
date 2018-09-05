---
UID: NF:d3d10effect.ID3D10EffectMatrixVariable.GetMatrixTranspose
title: ID3D10EffectMatrixVariable::GetMatrixTranspose
author: windows-sdk-content
description: Transpose and get a floating-point matrix.
old-location: direct3d10\id3d10effectmatrixvariable_getmatrixtranspose.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectmatrixvariable_getmatrixtranspose.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 417baa18-036a-1c79-9d4f-9e61637c5308, GetMatrixTranspose, GetMatrixTranspose method [Direct3D 10], GetMatrixTranspose method [Direct3D 10],ID3D10EffectMatrixVariable interface, ID3D10EffectMatrixVariable interface [Direct3D 10],GetMatrixTranspose method, ID3D10EffectMatrixVariable.GetMatrixTranspose, ID3D10EffectMatrixVariable::GetMatrixTranspose, d3d10effect/ID3D10EffectMatrixVariable::GetMatrixTranspose, direct3d10.id3d10effectmatrixvariable_getmatrixtranspose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectMatrixVariable.GetMatrixTranspose
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectMatrixVariable::GetMatrixTranspose


## -description


Transpose and get a floating-point matrix.


## -parameters




### -param pData [out]

Type: <b>float*</b>

A pointer to the first element of a transposed matrix.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).




## -see-also




<a href="https://msdn.microsoft.com/82ffcc6e-9a92-4d72-a397-0a66600ad508">ID3D10EffectMatrixVariable Interface</a>
 

 

