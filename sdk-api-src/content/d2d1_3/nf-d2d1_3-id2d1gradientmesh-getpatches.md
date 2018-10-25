---
UID: NF:d2d1_3.ID2D1GradientMesh.GetPatches
title: ID2D1GradientMesh::GetPatches
author: windows-sdk-content
description: Returns a subset of the patches that make up this gradient mesh.
old-location: direct2d\id2d1gradientmesh_getpatches.htm
tech.root: direct2d
ms.assetid: d3ef9370-fb9f-d55b-d910-7dd938ecf0b6
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetPatches, GetPatches method [Direct2D], GetPatches method [Direct2D],ID2D1GradientMesh interface, ID2D1GradientMesh interface [Direct2D],GetPatches method, ID2D1GradientMesh.GetPatches, ID2D1GradientMesh::GetPatches, d2d1_3/ID2D1GradientMesh::GetPatches, direct2d.id2d1gradientmesh_getpatches
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GradientMesh.GetPatches
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GradientMesh::GetPatches


## -description


Returns a subset of the patches that make up this gradient mesh.


## -parameters




### -param startIndex

Type: <b>UINT32</b>

Index of the first patch to return.


### -param patches

Type: <b><a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a>*</b>

A pointer to the array to be filled with the patch data.


### -param patchesCount

Type: <b>UINT32</b>

The number of patches to be returned.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/0c51da97-7b70-d828-2a4d-cb62ff378a56">ID2D1GradientMesh</a>
 

 

