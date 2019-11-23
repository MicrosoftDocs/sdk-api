---
UID: NF:d2d1.ID2D1RenderTarget.CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush)
title: ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush) (d2d1.h)

description: Creates a new ID2D1SolidColorBrush that has the specified color and opacity.
old-location: direct2d\ID2D1RenderTarget_CreateSolidColorBrush_ref_COLOR_F_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1SolidColorBrush.htm
tech.root: Direct2D
ms.assetid: c6597602-92b2-491c-b9f3-5a44a6980b80

ms.date: 12/05/2018
ms.keywords: CreateSolidColorBrush, CreateSolidColorBrush method [Direct2D], CreateSolidColorBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateSolidColorBrush method, ID2D1RenderTarget.CreateSolidColorBrush, ID2D1RenderTarget.CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush), ID2D1RenderTarget::CreateSolidColorBrush, ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush), d2d1/ID2D1RenderTarget::CreateSolidColorBrush, direct2d.ID2D1RenderTarget_CreateSolidColorBrush_ref_COLOR_F_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1SolidColorBrush
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1RenderTarget.CreateSolidColorBrush"
dev_langs:
 - c++
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
 - ID2D1RenderTarget.CreateSolidColorBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush)


## -description


Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush">ID2D1SolidColorBrush</a> that has the specified color and opacity.


## -parameters




### -param color [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a></b>

The red, green, blue, and alpha values of the brush's color.


### -param brushProperties [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a></b>

The base opacity of the brush.


### -param solidColorBrush [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush">ID2D1SolidColorBrush</a>**</b>

When this method returns, contains the address of a pointer to the new brush. This parameter is passed uninitialized.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/getting-started-with-direct2d">Direct2D QuickStart</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

