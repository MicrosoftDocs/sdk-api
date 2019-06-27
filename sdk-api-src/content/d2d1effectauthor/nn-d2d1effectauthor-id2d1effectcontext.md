---
UID: NN:d2d1effectauthor.ID2D1EffectContext
title: ID2D1EffectContext (d2d1effectauthor.h)
author: windows-sdk-content
description: Provides factory methods and other state management for effect and transform authors.
old-location: direct2d\id2d1contextinternal.htm
tech.root: Direct2D
ms.assetid: 6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1EffectContext, ID2D1EffectContext interface [Direct2D], ID2D1EffectContext interface [Direct2D],described, d2d1effectauthor/ID2D1EffectContext, direct2d.id2d1contextinternal
ms.topic: interface
f1_keywords: 
 - "d2d1effectauthor/ID2D1EffectContext"
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
 - ID2D1EffectContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1EffectContext interface


## -description


Provides factory methods and other state management for effect and transform authors.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1EffectContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1EffectContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1EffectContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport">CheckFeatureSupport</a>
</td>
<td align="left" width="63%">
This indicates whether an optional capability is supported by the D3D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform">CreateBlendTransform</a>
</td>
<td align="left" width="63%">
This creates a blend transform that can be inserted into a transform graph. 



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform">CreateBorderTransform</a>
</td>
<td align="left" width="63%">
Creates a transform that extends its input infinitely in every direction based on the passed in extend mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createboundsadjustmenttransform">CreateBoundsAdjustmentTransform</a>
</td>
<td align="left" width="63%">
Creates and returns a bounds adjustment  transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createcolorcontext">CreateColorContext</a>
</td>
<td align="left" width="63%">
Creates a color context from a color space.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createcolorcontextfromfilename">CreateColorContextFromFilename</a>
</td>
<td align="left" width="63%">
Creates a color context by loading it from the specified filename.  The profile bytes are the contents of the file specified by <i>filename</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createcolorcontextfromwiccolorcontext">CreateColorContextFromWicColorContext</a>
</td>
<td align="left" width="63%">
Creates a color context from an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>.  The <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">D2D1ColorContext</a> space of the resulting context varies, see Remarks for more info.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createeffect">CreateEffect</a>
</td>
<td align="left" width="63%">
Creates a Direct2D effect for the specified  class ID.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform">CreateOffsetTransform</a>
</td>
<td align="left" width="63%">
Creates and returns an offset transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createresourcetexture">CreateResourceTexture</a>
</td>
<td align="left" width="63%">
Creates or finds the given resource texture, depending on whether a resource id is specified. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect">CreateTransformNodeFromEffect</a>
</td>
<td align="left" width="63%">
Wraps an effect graph into a single transform node and then inserted into a transform graph. This allows an effect to aggregate other effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">CreateVertexBuffer</a>
</td>
<td align="left" width="63%">
Creates a vertex buffer or finds a standard vertex buffer and optionally initializes it with vertices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-findresourcetexture">FindResourceTexture</a>
</td>
<td align="left" width="63%">
Finds the given resource texture if it has already been created with <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createresourcetexture">ID2D1EffectContext::CreateResourceTexture</a> with the same GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-findvertexbuffer">FindVertexBuffer</a>
</td>
<td align="left" width="63%">
This finds the given vertex buffer if it has already been created with <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">ID2D1EffectContext::CreateVertexBuffer</a> with the same GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-getdpi">GetDpi</a>
</td>
<td align="left" width="63%">
Gets the unit mapping that an effect will use for properties that could be in either dots per inch (dpi) or pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-getmaximumsupportedfeaturelevel">GetMaximumSupportedFeatureLevel</a>
</td>
<td align="left" width="63%">
This indicates the maximum feature level from the provided list which is supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-isbufferprecisionsupported">IsBufferPrecisionSupported</a>
</td>
<td align="left" width="63%">
 Indicates whether the buffer precision is supported by the underlying Direct2D <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">device.</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-isshaderloaded">IsShaderLoaded</a>
</td>
<td align="left" width="63%">
This tests to see if the given shader is loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadcomputeshader">LoadComputeShader</a>
</td>
<td align="left" width="63%">
Loads the given shader by its unique ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader">LoadPixelShader</a>
</td>
<td align="left" width="63%">
Loads the given shader by its unique ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader">LoadVertexShader</a>
</td>
<td align="left" width="63%">
Loads the given shader by its unique ID.

</td>
</tr>
</table> 


## -remarks



This interface  is passed to an effect implementation through the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize">ID2D1EffectImpl::Initialize</a> method. In order to prevent applications casually gaining access to this interface, and to separate reference counts between the public and private interfaces, it is not possible to call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> between the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a> and the <b>ID2D1EffectContext</b>.

Each call to <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize">ID2D1Effect::Initialize</a> will be provided a different <b>ID2D1EffectContext</b> interface. This interface tracks resource allocations for the effect. When the effect is released, the corresponding allocations will also be released.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl">ID2D1EffectImpl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring">ID2D1Factory::RegisterEffect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

