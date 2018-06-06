---
UID: NN:mileffects.IMILBitmapEffect
title: IMILBitmapEffect
author: windows-sdk-content
description: Exposes methods that define a Windows Presentation Foundation (WPF) bitmap effect.
old-location: wibe\_wibe_imilbitmapeffect.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffect\imilbitmapeffect.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: IMILBitmapEffect, IMILBitmapEffect interface [WPF Bitmap Effects], IMILBitmapEffect interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffect, mileffects/IMILBitmapEffect, wibe._wibe_imilbitmapeffect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffect interface


## -description


Exposes methods that define a Windows Presentation Foundation (WPF) bitmap effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffect</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71285e15-85c5-4d0f-81d4-fd61cf621a36">GetOutput</a>
</td>
<td align="left" width="63%">
Gets the output of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7196b610-729a-4213-850e-b956497f695a">GetParentEffect</a>
</td>
<td align="left" width="63%">
Gets a parent of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/092c392f-e9b5-4ee5-bdfe-f378ceee2378">SetInputSource</a>
</td>
<td align="left" width="63%">
Sets the effect input source.

</td>
</tr>
</table> 


## -remarks



<b>IMILBitmapEffect</b> is a wrapper for a <a href="https://msdn.microsoft.com/23eea785-8545-44d3-bfcb-1ffbc82ecc6a">IMILBitmapEffectPrimitive</a>. A <b>IMILBitmapEffectPrimitive</b> is wrapped by a <b>IMILBitmapEffect</b> through Component Object Model (COM) aggregation.
            Therefore, independent software vendor (ISV) effect writers do not need to implement the <b>IMILBitmapEffect</b>, <a href="https://msdn.microsoft.com/22b71222-e572-42e2-af0d-dc7061eec5df">IMILBitmapEffectImpl</a>, and <a href="https://msdn.microsoft.com/befa56bb-149e-4a90-a1cb-9e61e7f5366c">IMILBitmapEffectConnections</a> interfaces.
         



