---
UID: NN:mileffects.IMILBitmapEffectRenderContextImpl
title: IMILBitmapEffectRenderContextImpl (mileffects.h)

description: Exposes methods that define a IMILBitmapEffectRenderContext.
old-location: wibe\_wibe_imilbitmapeffectrendercontextimpl.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontextimpl\imilbitmapeffectrendercontextimpl.htm

ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectRenderContextImpl, IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects], IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectrendercontextimpl, mileffects/IMILBitmapEffectRenderContextImpl, wibe._wibe_imilbitmapeffectrendercontextimpl
ms.topic: interface
f1_keywords: 
 - "mileffects/IMILBitmapEffectRenderContextImpl"
dev_langs:
 - c++
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mileffects.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectRenderContextImpl
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectRenderContextImpl interface


## -description


Exposes methods that define a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectrendercontext">IMILBitmapEffectRenderContext</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectRenderContextImpl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectRenderContextImpl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectRenderContextImpl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectrendercontextimpl-getoutputbounds">GetOutputBounds</a>
</td>
<td align="left" width="63%">
Gets the output bounds of the render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectrendercontextimpl-gettransform">GetTransform</a>
</td>
<td align="left" width="63%">
Gets the matrix transform of the render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectrendercontextimpl-getusesoftwarerenderer">GetUseSoftwareRenderer</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether to use software rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectrendercontextimpl-updateoutputbounds">UpdateOutputBounds</a>
</td>
<td align="left" width="63%">
Updates the output bounds with the given region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectrendercontextimpl-updatetransform">UpdateTransform</a>
</td>
<td align="left" width="63%">
Updates the output transform with the new matrix.

</td>
</tr>
</table> 

