---
UID: NF:d3d10effect.ID3D10EffectMatrixVariable.GetMatrixArray
title: ID3D10EffectMatrixVariable::GetMatrixArray (d3d10effect.h)
author: windows-sdk-content
description: Get an array of matrices.
old-location: direct3d10\id3d10effectmatrixvariable_getmatrixarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectmatrixvariable_getmatrixarray.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 84951199-eff7-9ce2-9bad-b1bc01eab150, GetMatrixArray, GetMatrixArray method [Direct3D 10], GetMatrixArray method [Direct3D 10],ID3D10EffectMatrixVariable interface, ID3D10EffectMatrixVariable interface [Direct3D 10],GetMatrixArray method, ID3D10EffectMatrixVariable.GetMatrixArray, ID3D10EffectMatrixVariable::GetMatrixArray, d3d10effect/ID3D10EffectMatrixVariable::GetMatrixArray, direct3d10.id3d10effectmatrixvariable_getmatrixarray
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectMatrixVariable.GetMatrixArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectMatrixVariable::GetMatrixArray


## -description


Get an array of matrices.


## -parameters




### -param pData [out]

Type: <b>float*</b>

A pointer to the first element of the first matrix in an array of matrices.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset (in number of matrices) between the start of the array and the first matrix returned.


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of matrices in the returned array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173647(v=VS.85).aspx">ID3D10EffectMatrixVariable Interface</a>
 

 

