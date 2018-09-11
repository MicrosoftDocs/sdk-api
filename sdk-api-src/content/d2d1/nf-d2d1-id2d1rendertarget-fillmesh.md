---
UID: NF:d2d1.ID2D1RenderTarget.FillMesh
title: ID2D1RenderTarget::FillMesh
author: windows-sdk-content
description: Paints the interior of the specified mesh.
old-location: direct2d\ID2D1RenderTarget_FillMesh.htm
tech.root: direct2d
ms.assetid: e22c9169-e770-4f3d-819b-b9363b6e6542
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FillMesh, FillMesh method [Direct2D], FillMesh method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillMesh method, ID2D1RenderTarget.FillMesh, ID2D1RenderTarget::FillMesh, d2d1/ID2D1RenderTarget::FillMesh, direct2d.ID2D1RenderTarget_FillMesh
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
 - ID2D1RenderTarget.FillMesh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::FillMesh


## -description


Paints the interior of the specified mesh.


## -parameters




### -param mesh [in]

Type: <b><a href="https://msdn.microsoft.com/2a58fb5f-2281-4f73-a689-cc1350d13c8b">ID2D1Mesh</a>*</b>

The mesh to paint.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the mesh.


## -returns



This method does not return a value.




## -remarks



The current antialias mode of the render target must be <a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE_ALIASED</a> when <b>FillMesh</b> is called. To change the render target's antialias mode, use the <a href="https://msdn.microsoft.com/cd727271-1725-48e1-be39-680b363db2ae">SetAntialiasMode</a> method.

<b>FillMesh</b> does not expect a particular winding order for the triangles in the <a href="https://msdn.microsoft.com/2a58fb5f-2281-4f73-a689-cc1350d13c8b">ID2D1Mesh</a>; both clockwise and counter-clockwise will work. 

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>FillMesh</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE_ALIASED</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/cd727271-1725-48e1-be39-680b363db2ae">SetAntialiasMode</a>
 

 

