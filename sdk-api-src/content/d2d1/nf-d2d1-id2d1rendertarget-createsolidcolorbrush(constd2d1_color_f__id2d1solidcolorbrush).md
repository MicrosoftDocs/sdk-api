---
UID: NF:d2d1.ID2D1RenderTarget.CreateSolidColorBrush(constD2D1_COLOR_F&,ID2D1SolidColorBrush)
title: ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &,ID2D1SolidColorBrush) (d2d1.h)
description: Creates a new ID2D1SolidColorBrush that has the specified color and a base opacity of 1.0f.
helpviewer_keywords: ["CreateSolidColorBrush","CreateSolidColorBrush method [Direct2D]","CreateSolidColorBrush method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateSolidColorBrush method","ID2D1RenderTarget.CreateSolidColorBrush","ID2D1RenderTarget.CreateSolidColorBrush(const D2D1_COLOR_F &","ID2D1SolidColorBrush)","ID2D1RenderTarget::CreateSolidColorBrush","ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &","ID2D1SolidColorBrush)","d2d1/ID2D1RenderTarget::CreateSolidColorBrush","direct2d.ID2D1RenderTarget_CreateSolidColorBrush_ref_COLOR_F_ptr_ptr_ID2D1SolidColorBrush"]
old-location: direct2d\ID2D1RenderTarget_CreateSolidColorBrush_ref_COLOR_F_ptr_ptr_ID2D1SolidColorBrush.htm
tech.root: Direct2D
ms.assetid: 67974629-5c34-4c94-acad-586849cdb880
ms.date: 12/05/2018
ms.keywords: CreateSolidColorBrush, CreateSolidColorBrush method [Direct2D], CreateSolidColorBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateSolidColorBrush method, ID2D1RenderTarget.CreateSolidColorBrush, ID2D1RenderTarget.CreateSolidColorBrush(const D2D1_COLOR_F &,ID2D1SolidColorBrush), ID2D1RenderTarget::CreateSolidColorBrush, ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &,ID2D1SolidColorBrush), d2d1/ID2D1RenderTarget::CreateSolidColorBrush, direct2d.ID2D1RenderTarget_CreateSolidColorBrush_ref_COLOR_F_ptr_ptr_ID2D1SolidColorBrush
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
 - ID2D1RenderTarget::CreateSolidColorBrush
 - d2d1/ID2D1RenderTarget::CreateSolidColorBrush
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
 - ID2D1RenderTarget.CreateSolidColorBrush
---

## -description

Creates a new <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush">ID2D1SolidColorBrush</a> that has the specified color and a base opacity of 1.0f.

## -parameters

### -param color

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-color-f">D2D1_COLOR_F</a> &</b>

The red, green, blue, and alpha values of the brush's color.

### -param solidColorBrush

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush">ID2D1SolidColorBrush</a>**</b>

When this method returns, contains the address of a pointer to the new brush. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>

<a href="/windows/win32/Direct2D/getting-started-with-direct2d">Direct2D QuickStart</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

