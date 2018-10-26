---
UID: NN:dxgi.IDXGISurface1
title: IDXGISurface1
author: windows-sdk-content
description: The IDXGISurface1 interface extends the IDXGISurface by adding support for using Windows Graphics Device Interface (GDI) to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface.
old-location: direct3ddxgi\idxgisurface1.htm
tech.root: direct3ddxgi
ms.assetid: 99ece4f3-1bad-46b8-94a9-6ef559864b1c
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: 3c2c6548-026c-d082-91b7-abb986ff3a00, IDXGISurface1, IDXGISurface1 interface [DXGI], IDXGISurface1 interface [DXGI],described, direct3ddxgi.idxgisurface1, dxgi/IDXGISurface1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGISurface1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISurface1 interface


## -description


The <b>IDXGISurface1</b> interface extends the <a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a> by adding support for using Windows Graphics Device Interface (GDI) to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISurface1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>. <b>IDXGISurface1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGISurface1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b148d2b4-36a2-46b9-8a98-9f3c478549a4">GetDC</a>
</td>
<td align="left" width="63%">
Returns a device context (DC) that allows you to render to a DXGI surface using GDI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c3a0cf3-c970-4908-a960-ba261756bd5f">ReleaseDC</a>
</td>
<td align="left" width="63%">
Releases the GDI device context (DC) that is associated with the current surface and allows you to use Direct3D to render.

</td>
</tr>
</table> 


## -remarks



This interface is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

An image-data object is a 2D section of memory, commonly called a surface. To get the surface from an output, call <a href="https://msdn.microsoft.com/en-us/library/Bb174550(v=VS.85).aspx">IDXGIOutput::GetDisplaySurfaceData</a>. Then, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a> object that <b>IDXGIOutput::GetDisplaySurfaceData</b> returns to retrieve the <b>IDXGISurface1</b> interface.

Any object that supports <a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a> also supports <b>IDXGISurface1</b>.

The runtime automatically creates an <b>IDXGISurface1</b> interface when it creates a Direct3D resource object that represents a surface. For example, the runtime creates an <b>IDXGISurface1</b> interface when you call <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb173560(v=VS.85).aspx">ID3D10Device::CreateTexture2D</a> to create a 2D texture. To retrieve the <b>IDXGISurface1</b> interface that represents the 2D texture surface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">ID3D11Texture2D::QueryInterface</a> or <b>ID3D10Texture2D::QueryInterface</b>. In this call, you must pass the identifier of <b>IDXGISurface1</b>. If the 2D texture has only a single MIP-map level and does not consist of an array of textures, <b>QueryInterface</b> succeeds and returns a pointer to the <b>IDXGISurface1</b> interface pointer. Otherwise, <b>QueryInterface</b> fails and does not return the pointer to <b>IDXGISurface1</b>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>
 

 

