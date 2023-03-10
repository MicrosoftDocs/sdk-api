---
UID: NF:d2d1effectauthor.ID2D1EffectImpl.PrepareForRender
title: ID2D1EffectImpl::PrepareForRender (d2d1effectauthor.h)
description: Prepares an effect for the rendering process.
helpviewer_keywords: ["ID2D1EffectImpl interface [Direct2D]","PrepareForRender method","ID2D1EffectImpl.PrepareForRender","ID2D1EffectImpl::PrepareForRender","PrepareForRender","PrepareForRender method [Direct2D]","PrepareForRender method [Direct2D]","ID2D1EffectImpl interface","d2d1effectauthor/ID2D1EffectImpl::PrepareForRender","direct2d.id2d1effectimpl_prepareforrender"]
old-location: direct2d\id2d1effectimpl_prepareforrender.htm
tech.root: Direct2D
ms.assetid: 0EBA4FDB-A9EA-4FCF-BF40-3D73ED356CD4
ms.date: 12/05/2018
ms.keywords: ID2D1EffectImpl interface [Direct2D],PrepareForRender method, ID2D1EffectImpl.PrepareForRender, ID2D1EffectImpl::PrepareForRender, PrepareForRender, PrepareForRender method [Direct2D], PrepareForRender method [Direct2D],ID2D1EffectImpl interface, d2d1effectauthor/ID2D1EffectImpl::PrepareForRender, direct2d.id2d1effectimpl_prepareforrender
req.header: d2d1effectauthor.h
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
req.lib: D2D1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectImpl::PrepareForRender
 - d2d1effectauthor/ID2D1EffectImpl::PrepareForRender
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectImpl.PrepareForRender
---

# ID2D1EffectImpl::PrepareForRender


## -description

Prepares an effect for the rendering process.

## -parameters

### -param changeType

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_change_type">D2D1_CHANGE_TYPE</a></b>

Indicates the type of change the effect should expect.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by the renderer when the effect is within an effect graph that is drawn.

 The method will be called:

<ul>
<li>If the effect has been initialized but has not previously been drawn.</li>
<li>If an effect property has been set since the last draw call.</li>
<li>If the context state has changed since the effect was last drawn.</li>
</ul>
The method will not otherwise be called. The transforms created by the effect will be called to handle their input and output rectangles for every draw call.

Most effects defer creating any resources or specifying a topology until this call is made. They store their properties and map them to a concrete set of rendering techniques when first drawn.


#### Examples

An effect normally waits until it is rendered before snapping its current state and applying it to any transforms it has encapsulated.


```cpp
class CMyTransform : public ID2D1DrawTransform
{
public:

    // Transform methods omitted.
    
    HRESULT PrepareForRender(FLOAT radius);
};

class CEffectImplementation : public ID2D1EffectImpl
{
public:

    void SetRadius(FLOAT radius) { _radius = radius; }

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE /*type*/)
    {
        // Send the radius to the transform and ask it to render.
        return _pMyTransform->PrepareForRender(_radius);
    }

private:

    CMyTransform *_pMyTransform;
    FLOAT _radius;
};

```

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl">ID2D1EffectImpl</a>