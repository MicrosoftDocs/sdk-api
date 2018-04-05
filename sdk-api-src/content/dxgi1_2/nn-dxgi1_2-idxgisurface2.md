---
UID: NN:dxgi1_2.IDXGISurface2
title: IDXGISurface2
author: windows-driver-content
description: The IDXGISurface2 interface extends the IDXGISurface1 interface by adding support for subresource surfaces and getting a handle to a shared resource.
old-location: direct3ddxgi\idxgisurface2.htm
old-project: direct3ddxgi
ms.assetid: EBBB2EE1-C5EA-4F98-AA8B-BCAA8C188F26
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDXGISurface2, IDXGISurface2 interface [DXGI], IDXGISurface2 interface [DXGI], described, direct3ddxgi.idxgisurface2, dxgi1_2/IDXGISurface2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dxgi.lib
-	Dxgi.dll
api_name:
-	IDXGISurface2
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISurface2 interface


## -description


The <b>IDXGISurface2</b> interface extends the <a href="https://msdn.microsoft.com/99ece4f3-1bad-46b8-94a9-6ef559864b1c">IDXGISurface1</a> interface by adding support for subresource surfaces and getting a handle to a shared resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISurface2</b> interface inherits from <a href="https://msdn.microsoft.com/99ece4f3-1bad-46b8-94a9-6ef559864b1c">IDXGISurface1</a>. <b>IDXGISurface2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGISurface2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0CDA5693-610F-4E7E-9540-353709E4FA8D">GetResource</a>
</td>
<td align="left" width="63%">
Gets the parent resource and subresource index that support a subresource surface.

</td>
</tr>
</table> 


## -remarks



An image-data object is a 2D section of memory, commonly called a surface. To get the surface from an output, call <a href="https://msdn.microsoft.com/c068853b-12dd-4175-b11a-06bef3b987b5">IDXGIOutput::GetDisplaySurfaceData</a>. Then, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a> object that <b>IDXGIOutput::GetDisplaySurfaceData</b> returns to retrieve the <b>IDXGISurface2</b> interface.

Any object that supports <a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a> also supports <b>IDXGISurface2</b>.

The runtime automatically creates an <b>IDXGISurface2</b> interface when it creates a Direct3D resource object that represents a surface. For example, the runtime creates an <b>IDXGISurface2</b> interface when you call <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a> to create a 2D texture. To retrieve the <b>IDXGISurface2</b> interface that represents the 2D texture surface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">ID3D11Texture2D::QueryInterface</a>. In this call, you must pass the identifier of <b>IDXGISurface2</b>. If the 2D texture has only a single MIP-map level and does not consist of an array of textures, <b>QueryInterface</b> succeeds and returns a pointer to the <b>IDXGISurface2</b> interface pointer. Otherwise, <b>QueryInterface</b> fails and does not return the pointer to <b>IDXGISurface2</b>.

You can call the <a href="https://msdn.microsoft.com/99730AB1-C5D9-41D6-8001-495FF26E8232">IDXGIResource1::CreateSubresourceSurface</a> method to create an <b>IDXGISurface2</b> interface that refers to one subresource of a stereo resource.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/99ece4f3-1bad-46b8-94a9-6ef559864b1c">IDXGISurface1</a>
 

 

