---
UID: NF:d2d1effectauthor.ID2D1EffectImpl.PrepareForRender
title: ID2D1EffectImpl::PrepareForRender
author: windows-sdk-content
description: Prepares an effect for the rendering process.
old-location: direct2d\id2d1effectimpl_prepareforrender.htm
tech.root: direct2d
ms.assetid: 0EBA4FDB-A9EA-4FCF-BF40-3D73ED356CD4
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID2D1EffectImpl interface [Direct2D],PrepareForRender method, ID2D1EffectImpl.PrepareForRender, ID2D1EffectImpl::PrepareForRender, PrepareForRender, PrepareForRender method [Direct2D], PrepareForRender method [Direct2D],ID2D1EffectImpl interface, d2d1effectauthor/ID2D1EffectImpl::PrepareForRender, direct2d.id2d1effectimpl_prepareforrender
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1effectauthor.h
: 
- ID2D1EffectImpl.PrepareForRender
: 
---

# ID2D1EffectImpl::PrepareForRender


## -description


Prepares an effect for the rendering process.


## -parameters




### -param changeType

Type: <b><a href="https://msdn.microsoft.com/22960a80-1986-4ca0-98df-87f05e880e98">D2D1_CHANGE_TYPE</a></b>

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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>class CMyTransform : public ID2D1DrawTransform
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
        return _pMyTransform-&gt;PrepareForRender(_radius);
    }

private:

    CMyTransform *_pMyTransform;
    FLOAT _radius;
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>
 

 

