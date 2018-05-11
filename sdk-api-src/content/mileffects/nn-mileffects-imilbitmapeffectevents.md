---
UID: NN:mileffects.IMILBitmapEffectEvents
title: IMILBitmapEffectEvents
author: windows-driver-content
description: Exposes methods that define an effect event.
old-location: wibe\_wibe_imilbitmapeffectevents.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectevents\imilbitmapeffectevents.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMILBitmapEffectEvents, IMILBitmapEffectEvents interface [WPF Bitmap Effects], IMILBitmapEffectEvents interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectevents, mileffects/IMILBitmapEffectEvents, wibe._wibe_imilbitmapeffectevents
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.dll
api_name:
-	IMILBitmapEffectEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectEvents interface


## -description


Exposes methods that define an effect event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4e7886ff-f211-4c9b-b57d-e1d24ca20bc2">DirtyRegion</a>
</td>
<td align="left" width="63%">
Invalidates the specified region of the given <a href="https://msdn.microsoft.com/23eea785-8545-44d3-bfcb-1ffbc82ecc6a">IMILBitmapEffectPrimitive</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5836de27-aea8-4366-9690-65e66e1418b4">PropertyChange</a>
</td>
<td align="left" width="63%">
Notifies an <a href="https://msdn.microsoft.com/23eea785-8545-44d3-bfcb-1ffbc82ecc6a">IMILBitmapEffectPrimitive</a> of a property change.

</td>
</tr>
</table> 

