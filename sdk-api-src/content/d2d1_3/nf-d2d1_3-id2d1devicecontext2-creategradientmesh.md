---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateGradientMesh
title: ID2D1DeviceContext2::CreateGradientMesh
author: windows-sdk-content
description: Creates a new ID2D1GradientMesh instance using the given array of patches.
old-location: direct2d\id2d1devicecontext2_creategradientmesh.htm
tech.root: Direct2D
ms.assetid: 7c471ba3-fb0f-b735-d10b-9d0a56b32863
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateGradientMesh, CreateGradientMesh method [Direct2D], CreateGradientMesh method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateGradientMesh method, ID2D1DeviceContext2.CreateGradientMesh, ID2D1DeviceContext2::CreateGradientMesh, d2d1_3/ID2D1DeviceContext2::CreateGradientMesh, direct2d.id2d1devicecontext2_creategradientmesh
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
 - ID2D1DeviceContext2.CreateGradientMesh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext2::CreateGradientMesh


## -description


Creates a new <a href="https://msdn.microsoft.com/0c51da97-7b70-d828-2a4d-cb62ff378a56">ID2D1GradientMesh</a> instance using the given array of patches.


## -parameters




### -param patches [in]

Type: <b>const <a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a>*</b>

A pointer to the array containing the patches to be used in this mesh.


### -param patchesCount

Type: <b>UINT32</b>

The number of patches in the patches argument to read.


### -param gradientMesh [out]

Type: <b><a href="https://msdn.microsoft.com/0c51da97-7b70-d828-2a4d-cb62ff378a56">ID2D1GradientMesh</a>**</b>

When this method returns, contains the address of a pointer to the new gradient mesh.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

