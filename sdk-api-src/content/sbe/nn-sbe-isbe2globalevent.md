---
UID: NN:sbe.ISBE2GlobalEvent
title: ISBE2GlobalEvent (sbe.h)
description: Offers access to global spanning events and their data from the Stream Buffer Source filters. A global spanning event contains state information that applies to all the streams in a pipeline.
old-location: mstv\isbe2globalevent.htm
tech.root: mstv
ms.assetid: 18bb9f8a-df97-468c-acb2-be7fa61a4789
ms.date: 12/05/2018
ms.keywords: ISBE2GlobalEvent, ISBE2GlobalEvent interface [Microsoft TV Technologies], ISBE2GlobalEvent interface [Microsoft TV Technologies],described, mstv.isbe2globalevent, sbe/ISBE2GlobalEvent
f1_keywords:
- sbe/ISBE2GlobalEvent
dev_langs:
- c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
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
- sbe.h
api_name:
- ISBE2GlobalEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISBE2GlobalEvent interface


## -description


Offers  access to global spanning events and their data from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filters.  A <i>global spanning event</i> contains state information that applies to all the streams in a pipeline.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2GlobalEvent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISBE2GlobalEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2GlobalEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2globalevent-getevent">GetEvent</a>
</td>
<td align="left" width="63%">
Gets an global spanning event and its data from a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2GlobalEvent)</code>.



