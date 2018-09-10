---
UID: NF:d3d10effect.ID3D10EffectMatrixVariable.SetMatrixArray
title: ID3D10EffectMatrixVariable::SetMatrixArray
author: windows-sdk-content
description: Set an array of floating-point matrices.
old-location: direct3d10\id3d10effectmatrixvariable_setmatrixarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectmatrixvariable_setmatrixarray.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ID3D10EffectMatrixVariable interface [Direct3D 10],SetMatrixArray method, ID3D10EffectMatrixVariable.SetMatrixArray, ID3D10EffectMatrixVariable::SetMatrixArray, SetMatrixArray, SetMatrixArray method [Direct3D 10], SetMatrixArray method [Direct3D 10],ID3D10EffectMatrixVariable interface, ba745b53-173b-3f99-1c4a-10c74d10a02b, d3d10effect/ID3D10EffectMatrixVariable::SetMatrixArray, direct3d10.id3d10effectmatrixvariable_setmatrixarray
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D10EffectMatrixVariable.SetMatrixArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectMatrixVariable::SetMatrixArray


## -description


Set an array of floating-point matrices.


## -parameters




### -param pData [in]

Type: <b>float*</b>

A pointer to the first matrix.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of matrix elements to skip from the start of the array.


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of elements to set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173647(v=VS.85).aspx">ID3D10EffectMatrixVariable Interface</a>
 

 

