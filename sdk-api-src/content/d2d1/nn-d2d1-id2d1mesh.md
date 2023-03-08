---
UID: NN:d2d1.ID2D1Mesh
title: ID2D1Mesh (d2d1.h)
description: Represents a set of vertices that form a list of triangles.
helpviewer_keywords: ["ID2D1Mesh","ID2D1Mesh interface [Direct2D]","ID2D1Mesh interface [Direct2D]","described","d2d1/ID2D1Mesh","direct2d.ID2D1Mesh"]
old-location: direct2d\ID2D1Mesh.htm
tech.root: Direct2D
ms.assetid: 2a58fb5f-2281-4f73-a689-cc1350d13c8b
ms.date: 12/05/2018
ms.keywords: ID2D1Mesh, ID2D1Mesh interface [Direct2D], ID2D1Mesh interface [Direct2D],described, d2d1/ID2D1Mesh, direct2d.ID2D1Mesh
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Mesh
 - d2d1/ID2D1Mesh
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Mesh
---

# ID2D1Mesh interface


## -description

Represents a set of vertices that form a list of triangles.

## -inheritance

The <b>ID2D1Mesh</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1Mesh</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

<h3><a id="Creating_ID2D1Mesh_Objects"></a><a id="creating_id2d1mesh_objects"></a><a id="CREATING_ID2D1MESH_OBJECTS"></a>Creating ID2D1Mesh Objects</h3>
To create a mesh, call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createmesh">ID2D1RenderTarget::CreateMesh</a> method on the render target with which the mesh will be used. A mesh can only be used with the render target that created it and the render target's compatible targets.

A mesh is a device-dependent resource: your application should create meshes after it initializes the render target with which the meshes will be used, and recreate the meshes whenever the render target needs recreated. (For more information about resources, see <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.)


## Examples

The following code example shows how to use <b>ID2D1Mesh</b>  to represent a set of vertices that form a list of triangles.  


```cpp
 ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry->Open(&pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry->Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink->Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT->CreateMesh(&pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh->Open(&pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry->Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink->Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink->Release();
                 }
                 pMesh->Release();
             }
         }
     }
     pGeometrySink->Release();
 }
 pPathGeometry->Release();

```


<div class="code"></div>

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

