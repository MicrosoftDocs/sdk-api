---
UID: NF:d3d11_1.ID3D11DeviceContext1.DiscardView
title: ID3D11DeviceContext1::DiscardView (d3d11_1.h)
description: Discards a resource view from the device context.
helpviewer_keywords: ["DiscardView","DiscardView method [Direct3D 11]","DiscardView method [Direct3D 11]","ID3D11DeviceContext1 interface","ID3D11DeviceContext1 interface [Direct3D 11]","DiscardView method","ID3D11DeviceContext1.DiscardView","ID3D11DeviceContext1::DiscardView","d3d11_1/ID3D11DeviceContext1::DiscardView","direct3d11.id3d11devicecontext1_discardview"]
old-location: direct3d11\id3d11devicecontext1_discardview.htm
tech.root: direct3d11
ms.assetid: 7BBF20BC-3777-46B9-8DE3-40B7B88DAF6C
ms.date: 12/05/2018
ms.keywords: DiscardView, DiscardView method [Direct3D 11], DiscardView method [Direct3D 11],ID3D11DeviceContext1 interface, ID3D11DeviceContext1 interface [Direct3D 11],DiscardView method, ID3D11DeviceContext1.DiscardView, ID3D11DeviceContext1::DiscardView, d3d11_1/ID3D11DeviceContext1::DiscardView, direct3d11.id3d11devicecontext1_discardview
req.header: d3d11_1.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext1::DiscardView
 - d3d11_1/ID3D11DeviceContext1::DiscardView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext1.DiscardView
---

# ID3D11DeviceContext1::DiscardView


## -description

Discards a resource view from the device context.

## -parameters

### -param pResourceView [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a> interface for the resource view to discard. The resource that underlies the view must have been created with usage <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DEFAULT</a> or <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DYNAMIC</a>, otherwise the runtime drops the call to <b>DiscardView</b>; if the debug layer is enabled, the runtime returns an error message.

## -remarks

<b>DiscardView</b> informs the graphics processing unit (GPU) that the existing content in the resource view that <i>pResourceView</i> points to is no longer needed.  The view can be an SRV, RTV, UAV, or DSV.  <b>DiscardView</b> is a variation on the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-discardresource">DiscardResource</a> method.  <b>DiscardView</b> allows you to discard a subset of a resource that is in a view (such as a single miplevel).  More importantly, <b>DiscardView</b> provides a convenience because often views are what are being bound and unbound at the pipeline.  Some pipeline bindings do not have views, such as stream output.  In that situation, <b>DiscardResource</b> can do the job for any resource.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>