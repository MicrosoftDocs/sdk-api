---
UID: NF:d2d1.ID2D1RenderTarget.CreateLayer(D2D1_SIZE_F,ID2D1Layer)
title: ID2D1RenderTarget::CreateLayer(D2D1_SIZE_F,ID2D1Layer) (d2d1.h)
description: Creates a layer resource that can be used with this render target and its compatible render targets. The new layer has the specified initial size.
helpviewer_keywords: ["CreateLayer","CreateLayer method [Direct2D]","CreateLayer method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateLayer method","ID2D1RenderTarget.CreateLayer","ID2D1RenderTarget.CreateLayer(D2D1_SIZE_F","ID2D1Layer)","ID2D1RenderTarget::CreateLayer","ID2D1RenderTarget::CreateLayer(D2D1_SIZE_F","ID2D1Layer)","d2d1/ID2D1RenderTarget::CreateLayer","direct2d.ID2D1RenderTarget_CreateLayer_D2D_SIZE_F_ptr_ptr_ID2D1Layer"]
old-location: direct2d\ID2D1RenderTarget_CreateLayer_D2D_SIZE_F_ptr_ptr_ID2D1Layer.htm
tech.root: Direct2D
ms.assetid: c21596a3-2b10-4a96-9a01-cf9325e51fe3
ms.date: 12/05/2018
ms.keywords: CreateLayer, CreateLayer method [Direct2D], CreateLayer method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateLayer method, ID2D1RenderTarget.CreateLayer, ID2D1RenderTarget.CreateLayer(D2D1_SIZE_F,ID2D1Layer), ID2D1RenderTarget::CreateLayer, ID2D1RenderTarget::CreateLayer(D2D1_SIZE_F,ID2D1Layer), d2d1/ID2D1RenderTarget::CreateLayer, direct2d.ID2D1RenderTarget_CreateLayer_D2D_SIZE_F_ptr_ptr_ID2D1Layer
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

Creates a layer resource that can be used with this render target and its compatible render targets. The new layer has the specified initial size.

## -parameters

### -param size

Type: [in] <b><a href="/windows/win32/Direct2D/d2d1-size-f">D2D1_SIZE_F</a></b>

If (0, 0) is specified, no backing store is created behind the layer resource. The layer resource is allocated to the minimum size when <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> is called.

### -param layer

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1layer">ID2D1Layer</a>**</b>

When the method returns, contains a pointer to a pointer to the new layer. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

Regardless of whether a size is initially specified, the layer automatically resizes as needed.

## Examples

For an example on how to use [CreateLayer](./nf-d2d1-id2d1rendertarget-createlayer(constd2d1_size_f_id2d1layer).md), see the <a href="/windows/win32/Direct2D/how-to-clip-with-layers">How to Clip a Region with a Layer</a> topic.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

<a href="/windows/win32/Direct2D/direct2d-layers-overview">Layers Overview</a>