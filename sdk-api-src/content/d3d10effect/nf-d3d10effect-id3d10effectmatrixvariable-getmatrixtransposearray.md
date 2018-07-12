---
UID: NF:d3d10effect.ID3D10EffectMatrixVariable.GetMatrixTransposeArray
title: ID3D10EffectMatrixVariable::GetMatrixTransposeArray
author: windows-sdk-content
description: Transpose and get an array of floating-point matrices.
old-location: direct3d10\id3d10effectmatrixvariable_getmatrixtransposearray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectmatrixvariable_getmatrixtransposearray.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 97f65a10-d90a-eb86-1a16-97e8d6e33352, GetMatrixTransposeArray, GetMatrixTransposeArray method [Direct3D 10], GetMatrixTransposeArray method [Direct3D 10],ID3D10EffectMatrixVariable interface, ID3D10EffectMatrixVariable interface [Direct3D 10],GetMatrixTransposeArray method, ID3D10EffectMatrixVariable.GetMatrixTransposeArray, ID3D10EffectMatrixVariable::GetMatrixTransposeArray, d3d10effect/ID3D10EffectMatrixVariable::GetMatrixTransposeArray, direct3d10.id3d10effectmatrixvariable_getmatrixtransposearray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectMatrixVariable.GetMatrixTransposeArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectMatrixVariable::GetMatrixTransposeArray


## -description


Transpose and get an array of floating-point matrices.


## -parameters




### -param pData [out]

Type: <b>float*</b>

A pointer to the first element of an array of tranposed matrices.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset (in number of matrices) between the start of the array and the first matrix to get.


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of matrices in the array to get.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173647(v=VS.85).aspx">ID3D10EffectMatrixVariable Interface</a>
 

 

