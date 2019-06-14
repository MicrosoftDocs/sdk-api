---
UID: NN:mileffects.IMILBitmapEffectImpl
title: IMILBitmapEffectImpl (mileffects.h)
author: windows-sdk-content
description: Exposes methods that define an an out IMILBitmapEffect object.
old-location: wibe\_wibe_imilbitmapeffectimpl.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\imilbitmapeffectimpl.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectImpl, IMILBitmapEffectImpl interface [WPF Bitmap Effects], IMILBitmapEffectImpl interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectimpl, mileffects/IMILBitmapEffectImpl, wibe._wibe_imilbitmapeffectimpl
ms.topic: interface
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
 - IMILBitmapEffectImpl
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectImpl interface


## -description


Exposes methods that define an an out <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectImpl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectImpl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectImpl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectimpl-getinputbitmapsource">GetInputBitmapSource</a>
</td>
<td align="left" width="63%">
Gets the input bitmap source of the effect of the given render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectimpl-getinputsource">GetInputSource</a>
</td>
<td align="left" width="63%">
Retrieves the input <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource Interface</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectimpl-getinputsourcebounds">GetInputSourceBounds</a>
</td>
<td align="left" width="63%">
Gets the bounds of the input source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectimpl-getoutputbitmapsource">GetOutputBitmapSource</a>
</td>
<td align="left" width="63%">
Gets the output bitmap source of the effect of the given render context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectimpl-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the effect with the given object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectimpl-isinplacemodificationallowed">IsInPlaceModificationAllowed</a>
</td>
<td align="left" width="63%">
Determines whether the effect allows in-place modifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectimpl-setparenteffect">SetParentEffect</a>
</td>
<td align="left" width="63%">
Sets the parent of the effect.

</td>
</tr>
</table> 


## -remarks



This interface must be implemented if a custom effect also exposes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a>.



