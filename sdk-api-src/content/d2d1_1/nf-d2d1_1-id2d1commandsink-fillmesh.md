---
UID: NF:d2d1_1.ID2D1CommandSink.FillMesh
title: ID2D1CommandSink::FillMesh
author: windows-sdk-content
description: Indicates a mesh to be filled by the command sink.
old-location: direct2d\id2d1commandsink_fillmesh.htm
tech.root: Direct2D
ms.assetid: b81ac1d2-06bb-4d39-b03d-c0abf7267c3a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FillMesh, FillMesh method [Direct2D], FillMesh method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],FillMesh method, ID2D1CommandSink.FillMesh, ID2D1CommandSink::FillMesh, d2d1_1/ID2D1CommandSink::FillMesh, direct2d.id2d1commandsink_fillmesh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1CommandSink.FillMesh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::FillMesh


## -description


Indicates a mesh to be filled by the command sink.


## -parameters




### -param mesh [in]

Type: <b><a href="https://msdn.microsoft.com/2a58fb5f-2281-4f73-a689-cc1350d13c8b">ID2D1Mesh</a>*</b>

The mesh object to be filled.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush with which to fill the mesh.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/e22c9169-e770-4f3d-819b-b9363b6e6542">ID2D1RenderTarget::FillMesh</a>
 

 

