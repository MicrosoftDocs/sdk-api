---
UID: NN:mileffects.IMILBitmapEffectPrimitiveImpl
title: IMILBitmapEffectPrimitiveImpl (mileffects.h)
author: windows-sdk-content
description: Exposes methods that report the state of a bitmap effect. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.
old-location: wibe\_wibe_imilbitmapeffectprimitiveimpl.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitiveimpl\imilbitmapeffectprimitiveimpl.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectPrimitiveImpl, IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects], IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectprimitiveimpl, mileffects/IMILBitmapEffectPrimitiveImpl, wibe._wibe_imilbitmapeffectprimitiveimpl
ms.topic: interface
f1_keywords: 
 - "mileffects/IMILBitmapEffectPrimitiveImpl"
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectPrimitiveImpl
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectPrimitiveImpl interface


## -description


Exposes methods that report the state of a bitmap effect. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectPrimitiveImpl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectPrimitiveImpl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectPrimitiveImpl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectprimitiveimpl-isdirty">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether the effect needs to be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectprimitiveimpl-isvolatile">IsVolatile</a>
</td>
<td align="left" width="63%">
Determines whether the current effect is considered volatile. If an effect is volatile, the effects framework will not attempt to cache the effect's output.

</td>
</tr>
</table> 

