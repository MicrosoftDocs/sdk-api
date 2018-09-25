---
UID: NF:d2d1.ID2D1RenderTarget.CreateMesh
title: ID2D1RenderTarget::CreateMesh
author: windows-sdk-content
description: Create a mesh that uses triangles to describe a shape.
old-location: direct2d\ID2D1RenderTarget_CreateMesh.htm
tech.root: direct2d
ms.assetid: 6c0036d8-1f91-4d90-a301-b58bde8da974
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CreateMesh, CreateMesh method [Direct2D], CreateMesh method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateMesh method, ID2D1RenderTarget.CreateMesh, ID2D1RenderTarget::CreateMesh, d2d1/ID2D1RenderTarget::CreateMesh, direct2d.ID2D1RenderTarget_CreateMesh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
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
 - ID2D1RenderTarget.CreateMesh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateMesh


## -description


Create a mesh that uses triangles to describe a shape.


## -parameters




### -param mesh [out]

Type: <b><a href="https://msdn.microsoft.com/2a58fb5f-2281-4f73-a689-cc1350d13c8b">ID2D1Mesh</a>**</b>

When this method returns, contains a pointer to a pointer to the new mesh.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To populate a mesh, use its <a href="https://msdn.microsoft.com/7cd0d637-7fcd-45a5-932f-5aa8fb476f68">Open</a> method to obtain an <a href="https://msdn.microsoft.com/967c702f-d16f-4a8e-ac77-a8bb35afe0a1">ID2D1TessellationSink</a>. To draw the mesh, use the render target's <a href="https://msdn.microsoft.com/e22c9169-e770-4f3d-819b-b9363b6e6542">FillMesh</a> method.




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

