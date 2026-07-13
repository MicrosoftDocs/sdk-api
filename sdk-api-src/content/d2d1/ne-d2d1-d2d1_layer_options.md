---
UID: NE:d2d1.D2D1_LAYER_OPTIONS
title: D2D1_LAYER_OPTIONS (d2d1.h)
description: Specifies options that can be applied when a layer resource is applied to create a layer.
helpviewer_keywords: ["D2D1_LAYER_OPTIONS","D2D1_LAYER_OPTIONS enumeration [Direct2D]","D2D1_LAYER_OPTIONS_INITIALIZE_FOR_CLEARTYPE","D2D1_LAYER_OPTIONS_NONE","d2d1/D2D1_LAYER_OPTIONS","d2d1/D2D1_LAYER_OPTIONS_INITIALIZE_FOR_CLEARTYPE","d2d1/D2D1_LAYER_OPTIONS_NONE","direct2d.D2D1_LAYER_OPTIONS"]
old-location: direct2d\D2D1_LAYER_OPTIONS.htm
tech.root: Direct2D
ms.assetid: d278211a-e99c-429d-9752-45c305f52ed8
ms.date: 12/05/2018
ms.keywords: D2D1_LAYER_OPTIONS, D2D1_LAYER_OPTIONS enumeration [Direct2D], D2D1_LAYER_OPTIONS_INITIALIZE_FOR_CLEARTYPE, D2D1_LAYER_OPTIONS_NONE, d2d1/D2D1_LAYER_OPTIONS, d2d1/D2D1_LAYER_OPTIONS_INITIALIZE_FOR_CLEARTYPE, d2d1/D2D1_LAYER_OPTIONS_NONE, direct2d.D2D1_LAYER_OPTIONS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_LAYER_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_LAYER_OPTIONS
 - d2d1/D2D1_LAYER_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_LAYER_OPTIONS
---

# D2D1_LAYER_OPTIONS enumeration


## -description

Specifies options that can be applied when a layer resource is applied to create a layer. 
<div class="alert"><b>Note</b>  Starting in Windows 8, the <b>D2D1_LAYER_OPTIONS_INITIALIZE_FOR_CLEARTYPE</b> option is no longer supported.  See <a href="/windows/win32/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1">D2D1_LAYER_OPTIONS1</a> for Windows 8 layer options.</div><div> </div>

## -enum-fields

### -field D2D1_LAYER_OPTIONS_NONE:0x00000000

The text in this layer does not use ClearType antialiasing.

### -field D2D1_LAYER_OPTIONS_INITIALIZE_FOR_CLEARTYPE:0x00000001

The layer renders correctly for ClearType text. If the render target is set to ClearType, the  layer continues to render ClearType. If the render target is set to ClearType and this option is not specified, the render target will be set to render gray-scale until the layer is popped. The caller can override this default by calling <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">SetTextAntialiasMode</a> while within the layer. This flag is slightly slower than the default.

### -field D2D1_LAYER_OPTIONS_FORCE_DWORD:0xffffffff

## -remarks

ClearType antialiasing must use the current contents of the render target to blend properly. When a pushed layer requests initializing for ClearType, Direct2D copies the current contents of the render target into the layer so that ClearType antialiasing can be performed. Rendering ClearType text into a transparent layer does not produce the desired results.

A small performance hit from re-copying content occurs when <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_)">ID2D1RenderTarget::Clear</a> is called.


## Examples

The following example shows how to use <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)">CreateLayer</a>, PushLayer, and <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a>. All fields in the  <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_layer_parameters">D2D1_LAYER_PARAMETERS</a> structure set to  defaults, except <b>opacityBrush</b>, which is set to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>.


```cpp
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);

```


For additional examples, see the <a href="/windows/win32/Direct2D/direct2d-layers-overview">Layers Overview</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/direct2d-layers-overview">Layers Overview</a>

