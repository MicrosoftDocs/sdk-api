---
UID: NN:mileffects.IMILBitmapEffects
title: IMILBitmapEffects (mileffects.h)
description: Exposes methods that define an enumeration of effects.
helpviewer_keywords: ["IMILBitmapEffects","IMILBitmapEffects interface [WPF Bitmap Effects]","IMILBitmapEffects interface [WPF Bitmap Effects]","described","_wibe_imilbitmapeffects","mileffects/IMILBitmapEffects","wibe._wibe_imilbitmapeffects"]
old-location: wibe\_wibe_imilbitmapeffects.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffects\imilbitmapeffects.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffects, IMILBitmapEffects interface [WPF Bitmap Effects], IMILBitmapEffects interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffects, mileffects/IMILBitmapEffects, wibe._wibe_imilbitmapeffects
f1_keywords:
- mileffects/IMILBitmapEffects
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
- IMILBitmapEffects
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffects interface


## -description


Exposes methods that define an enumeration of effects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffects</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffects</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffects</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/mileffects/nf-mileffects-imilbitmapeffects-_newenum">_NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves a new enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffects-get_count">Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffects-item">Item</a>
</td>
<td align="left" width="63%">
Retrieves the effect at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffects-get_parent">Parent</a>
</td>
<td align="left" width="63%">
Retrieves the parent effect group of enumeration.

</td>
</tr>
</table> 

