---
UID: NN:d2d1.ID2D1Mesh
title: ID2D1Mesh
author: windows-sdk-content
description: Represents a set of vertices that form a list of triangles.
old-location: direct2d\ID2D1Mesh.htm
tech.root: direct2d
ms.assetid: 2a58fb5f-2281-4f73-a689-cc1350d13c8b
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ID2D1Mesh, ID2D1Mesh interface [Direct2D], ID2D1Mesh interface [Direct2D],described, d2d1/ID2D1Mesh, direct2d.ID2D1Mesh
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID2D1Mesh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Mesh interface


## -description


Represents a set of vertices that form a list of triangles. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Mesh</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1Mesh</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Mesh</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cd0d637-7fcd-45a5-932f-5aa8fb476f68">Open</a>
</td>
<td align="left" width="63%">
Opens the mesh for population.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1Mesh_Objects"></a><a id="creating_id2d1mesh_objects"></a><a id="CREATING_ID2D1MESH_OBJECTS"></a>Creating ID2D1Mesh Objects</h3>
To create a mesh, call the <a href="https://msdn.microsoft.com/6c0036d8-1f91-4d90-a301-b58bde8da974">ID2D1RenderTarget::CreateMesh</a> method on the render target with which the mesh will be used. A mesh can only be used with the render target that created it and the render target's compatible targets.

A mesh is a device-dependent resource: your application should create meshes after it initializes the render target with which the meshes will be used, and recreate the meshes whenever the render target needs recreated. (For more information about resources, see <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.)


#### Examples

The following code example shows how to use <b>ID2D1Mesh</b>  to represent a set of vertices that form a list of triangles.  

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre> ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry-&gt;Open(&amp;pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry-&gt;Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink-&gt;Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT-&gt;CreateMesh(&amp;pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh-&gt;Open(&amp;pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry-&gt;Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink-&gt;Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&amp;m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink-&gt;Release();
                 }
                 pMesh-&gt;Release();
             }
         }
     }
     pGeometrySink-&gt;Release();
 }
 pPathGeometry-&gt;Release();
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

