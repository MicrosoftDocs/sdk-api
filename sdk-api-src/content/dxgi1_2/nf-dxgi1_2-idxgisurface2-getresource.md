---
UID: NF:dxgi1_2.IDXGISurface2.GetResource
title: IDXGISurface2::GetResource (dxgi1_2.h)
description: Gets the parent resource and subresource index that support a subresource surface.
helpviewer_keywords: ["GetResource","GetResource method [DXGI]","GetResource method [DXGI]","IDXGISurface2 interface","IDXGISurface2 interface [DXGI]","GetResource method","IDXGISurface2.GetResource","IDXGISurface2::GetResource","direct3ddxgi.idxgisurface2_getresource","dxgi1_2/IDXGISurface2::GetResource"]
old-location: direct3ddxgi\idxgisurface2_getresource.htm
tech.root: direct3ddxgi
ms.assetid: 0CDA5693-610F-4E7E-9540-353709E4FA8D
ms.date: 12/05/2018
ms.keywords: GetResource, GetResource method [DXGI], GetResource method [DXGI],IDXGISurface2 interface, IDXGISurface2 interface [DXGI],GetResource method, IDXGISurface2.GetResource, IDXGISurface2::GetResource, direct3ddxgi.idxgisurface2_getresource, dxgi1_2/IDXGISurface2::GetResource
req.header: dxgi1_2.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISurface2::GetResource
 - dxgi1_2/IDXGISurface2::GetResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISurface2.GetResource
---

# IDXGISurface2::GetResource


## -description

Gets the parent resource and subresource index that support a subresource surface.

## -parameters

### -param riid [in]

The globally unique identifier (GUID)  of the requested interface type.

### -param ppParentResource [out]

A pointer to a buffer that receives a pointer to the parent resource object for the subresource surface.

### -param pSubresourceIndex [out]

A pointer to a variable that receives the index of the subresource surface.

## -returns

Returns S_OK if successful; otherwise, returns one of the following values:

<ul>
<li>E_NOINTERFACE if the object does not implement the GUID that the <i>riid</i> parameter specifies.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -remarks

For subresource surface objects that the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface">IDXGIResource1::CreateSubresourceSurface</a> method creates, <b>GetResource</b> simply returns the values that were used to create the subresource surface.

Current objects that implement <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> are either resources or views.  <b>GetResource</b> for these objects returns “this” or the resource that supports the view respectively.  In this situation, the subresource index is 0.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2">IDXGISurface2</a>