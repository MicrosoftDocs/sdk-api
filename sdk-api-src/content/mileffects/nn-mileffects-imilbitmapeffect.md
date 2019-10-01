---
UID: NN:mileffects.IMILBitmapEffect
title: IMILBitmapEffect (mileffects.h)
author: windows-sdk-content
description: Exposes methods that define a Windows Presentation Foundation (WPF) bitmap effect.
old-location: wibe\_wibe_imilbitmapeffect.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffect\imilbitmapeffect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffect, IMILBitmapEffect interface [WPF Bitmap Effects], IMILBitmapEffect interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffect, mileffects/IMILBitmapEffect, wibe._wibe_imilbitmapeffect
ms.topic: interface
f1_keywords: 
 - "mileffects/IMILBitmapEffect"
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
 - IMILBitmapEffect
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffect interface


## -description


Exposes methods that define a Windows Presentation Foundation (WPF) bitmap effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffect</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffect</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffect-getoutput">GetOutput</a>
</td>
<td align="left" width="63%">
Gets the output of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffect-getparenteffect">GetParentEffect</a>
</td>
<td align="left" width="63%">
Gets a parent of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffect-setinputsource">SetInputSource</a>
</td>
<td align="left" width="63%">
Sets the effect input source.

</td>
</tr>
</table> 


## -remarks



<b>IMILBitmapEffect</b> is a wrapper for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectprimitive">IMILBitmapEffectPrimitive</a>. A <b>IMILBitmapEffectPrimitive</b> is wrapped by a <b>IMILBitmapEffect</b> through Component Object Model (COM) aggregation.
            Therefore, independent software vendor (ISV) effect writers do not need to implement the <b>IMILBitmapEffect</b>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectimpl">IMILBitmapEffectImpl</a>, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnections">IMILBitmapEffectConnections</a> interfaces.
         



