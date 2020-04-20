---
UID: NN:mileffects.IMILBitmapEffectEvents
title: IMILBitmapEffectEvents (mileffects.h)
description: Exposes methods that define an effect event.helpviewer_keywords: ["IMILBitmapEffectEvents","IMILBitmapEffectEvents interface [WPF Bitmap Effects]","IMILBitmapEffectEvents interface [WPF Bitmap Effects]","described","_wibe_imilbitmapeffectevents","mileffects/IMILBitmapEffectEvents","wibe._wibe_imilbitmapeffectevents"]
old-location: wibe\_wibe_imilbitmapeffectevents.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectevents\imilbitmapeffectevents.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectEvents, IMILBitmapEffectEvents interface [WPF Bitmap Effects], IMILBitmapEffectEvents interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectevents, mileffects/IMILBitmapEffectEvents, wibe._wibe_imilbitmapeffectevents
f1_keywords:
- mileffects/IMILBitmapEffectEvents
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
- IMILBitmapEffectEvents
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectEvents interface


## -description


Exposes methods that define an effect event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectevents-dirtyregion">DirtyRegion</a>
</td>
<td align="left" width="63%">
Invalidates the specified region of the given <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectprimitive">IMILBitmapEffectPrimitive</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectevents-propertychange">PropertyChange</a>
</td>
<td align="left" width="63%">
Notifies an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectprimitive">IMILBitmapEffectPrimitive</a> of a property change.

</td>
</tr>
</table> 

