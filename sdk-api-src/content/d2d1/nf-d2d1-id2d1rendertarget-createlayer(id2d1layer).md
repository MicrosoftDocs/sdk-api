---
UID: NF:d2d1.ID2D1RenderTarget.CreateLayer(ID2D1Layer)
title: ID2D1RenderTarget::CreateLayer(ID2D1Layer) (d2d1.h)
description: Creates a layer resource that can be used with this render target and its compatible render targets. (overload 1/2)
helpviewer_keywords: ["CreateLayer","CreateLayer method [Direct2D]","CreateLayer method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateLayer method","ID2D1RenderTarget.CreateLayer","ID2D1RenderTarget.CreateLayer(ID2D1Layer)","ID2D1RenderTarget::CreateLayer","ID2D1RenderTarget::CreateLayer(ID2D1Layer)","d2d1/ID2D1RenderTarget::CreateLayer","direct2d.ID2D1RenderTarget_CreateLayer_ptr_ptr_ID2D1Layer"]
old-location: direct2d\ID2D1RenderTarget_CreateLayer_ptr_ptr_ID2D1Layer.htm
tech.root: Direct2D
ms.assetid: 6a3377fb-f847-454f-9716-70a7b65fe96c
ms.date: 12/05/2018
ms.keywords: CreateLayer, CreateLayer method [Direct2D], CreateLayer method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateLayer method, ID2D1RenderTarget.CreateLayer, ID2D1RenderTarget.CreateLayer(ID2D1Layer), ID2D1RenderTarget::CreateLayer, ID2D1RenderTarget::CreateLayer(ID2D1Layer), d2d1/ID2D1RenderTarget::CreateLayer, direct2d.ID2D1RenderTarget_CreateLayer_ptr_ptr_ID2D1Layer
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
 - ID2D1RenderTarget::CreateLayer
 - d2d1/ID2D1RenderTarget::CreateLayer
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
 - ID2D1RenderTarget.CreateLayer
---

## -description

Creates a layer resource that can be used with this render target and its compatible render targets.

## -parameters

### -param layer

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1layer">ID2D1Layer</a>**</b>

When the method returns, contains a pointer to a pointer to the new layer. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

The layer automatically resizes itself, as needed.  

## Examples

For an example on how to use [CreateLayer](./nf-d2d1-id2d1rendertarget-createlayer(constd2d1_size_f_id2d1layer).md), see the <a href="/windows/win32/Direct2D/how-to-clip-with-layers">How to Clip a Region with a Layer</a>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

<a href="/windows/win32/Direct2D/direct2d-layers-overview">Layers Overview</a>
