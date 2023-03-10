---
UID: NF:d3d11_1.ID3D11DeviceContext1.DiscardView1
title: ID3D11DeviceContext1::DiscardView1 (d3d11_1.h)
description: Discards the specified elements in a resource view from the device context.
helpviewer_keywords: ["DiscardView1","DiscardView1 method [Direct3D 11]","DiscardView1 method [Direct3D 11]","ID3D11DeviceContext1 interface","ID3D11DeviceContext1 interface [Direct3D 11]","DiscardView1 method","ID3D11DeviceContext1.DiscardView1","ID3D11DeviceContext1::DiscardView1","d3d11_1/ID3D11DeviceContext1::DiscardView1","direct3d11.id3d11devicecontext1_discardview1"]
old-location: direct3d11\id3d11devicecontext1_discardview1.htm
tech.root: direct3d11
ms.assetid: C478F696-D0D7-4ABB-8BCD-5C528CC13814
ms.date: 12/05/2018
ms.keywords: DiscardView1, DiscardView1 method [Direct3D 11], DiscardView1 method [Direct3D 11],ID3D11DeviceContext1 interface, ID3D11DeviceContext1 interface [Direct3D 11],DiscardView1 method, ID3D11DeviceContext1.DiscardView1, ID3D11DeviceContext1::DiscardView1, d3d11_1/ID3D11DeviceContext1::DiscardView1, direct3d11.id3d11devicecontext1_discardview1
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
 - ID3D11DeviceContext1::DiscardView1
 - d3d11_1/ID3D11DeviceContext1::DiscardView1
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
 - ID3D11DeviceContext1.DiscardView1
---

# ID3D11DeviceContext1::DiscardView1


## -description

Discards the specified elements in a resource view from the device context.

## -parameters

### -param pResourceView [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a> interface for the resource view to discard. The resource that underlies the view must have been created with usage <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DEFAULT</a> or <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DYNAMIC</a>, otherwise the runtime drops the call to <b>DiscardView1</b>; if the debug layer is enabled, the runtime returns an error message.

### -param pRects [in, optional]

Type: <b>const <a href="/windows/desktop/direct3d11/d3d11-rect">D3D11_RECT</a>*</b>

An array of <a href="/windows/desktop/direct3d11/d3d11-rect">D3D11_RECT</a> structures for the rectangles in the resource view to discard. If <b>NULL</b>, <b>DiscardView1</b> discards the entire view and behaves the same as <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-discardview">DiscardView</a>.

### -param NumRects

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of rectangles in the array that the  <i>pRects</i> parameter specifies.

## -remarks

<b>DiscardView1</b> informs the graphics processing unit (GPU) that the existing content in the specified elements in the resource view that <i>pResourceView</i> points to is no longer needed.  The view can be an SRV, RTV, UAV, or DSV.  <b>DiscardView1</b> is a variation on the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-discardresource">DiscardResource</a> method.  <b>DiscardView1</b> allows you to discard elements of a subset of a resource that is in a view (such as elements of a single miplevel).  More importantly, <b>DiscardView1</b> provides a convenience because often views are what are being bound and unbound at the pipeline.  Some pipeline bindings do not have views, such as stream output.  In that situation, <b>DiscardResource</b> can do the job for any resource.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>