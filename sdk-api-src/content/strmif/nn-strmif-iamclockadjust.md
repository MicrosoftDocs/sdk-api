---
UID: NN:strmif.IAMClockAdjust
title: IAMClockAdjust (strmif.h)
description: The IAMClockAdjust interface adjusts the reference clock. The System Reference Clock exposes this interface.
helpviewer_keywords: ["IAMClockAdjust","IAMClockAdjust interface [DirectShow]","IAMClockAdjust interface [DirectShow]","described","IAMClockAdjustInterface","dshow.iamclockadjust","strmif/IAMClockAdjust"]
old-location: dshow\iamclockadjust.htm
tech.root: dshow
ms.assetid: e24105a5-711a-498a-a07c-842307602613
ms.date: 12/05/2018
ms.keywords: IAMClockAdjust, IAMClockAdjust interface [DirectShow], IAMClockAdjust interface [DirectShow],described, IAMClockAdjustInterface, dshow.iamclockadjust, strmif/IAMClockAdjust
f1_keywords:
- strmif/IAMClockAdjust
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMClockAdjust
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMClockAdjust interface


## -description



The <code>IAMClockAdjust</code> interface adjusts the reference clock. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/system-reference-clock">System Reference Clock</a> exposes this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMClockAdjust</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMClockAdjust</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMClockAdjust</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamclockadjust-setclockdelta">SetClockDelta</a>
</td>
<td align="left" width="63%">
Adjusts the clock time.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

