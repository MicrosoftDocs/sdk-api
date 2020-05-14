---
UID: NN:sbe.ISBE2GlobalEvent2
title: ISBE2GlobalEvent2 (sbe.h)
description: Offers access to global spanning events and their data from the Stream Buffer Source filters. A global spanning event contains state information that applies to all the streams in a pipeline. This interface extends the ISBE2GlobalEvent interface.helpviewer_keywords: ["ISBE2GlobalEvent2","ISBE2GlobalEvent2 interface [Microsoft TV Technologies]","ISBE2GlobalEvent2 interface [Microsoft TV Technologies]","described","mstv.isbe2globalevent2","sbe/ISBE2GlobalEvent2"]
old-location: mstv\isbe2globalevent2.htm
tech.root: mstv
ms.assetid: d03b2f9d-560d-4357-9388-ed287f4cc8db
ms.date: 12/05/2018
ms.keywords: ISBE2GlobalEvent2, ISBE2GlobalEvent2 interface [Microsoft TV Technologies], ISBE2GlobalEvent2 interface [Microsoft TV Technologies],described, mstv.isbe2globalevent2, sbe/ISBE2GlobalEvent2
f1_keywords:
- sbe/ISBE2GlobalEvent2
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
- ISBE2GlobalEvent2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISBE2GlobalEvent2 interface


## -description


Offers  access to global spanning events and their data from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filters.  A <i>global spanning event</i> contains state information that applies to all the streams in a pipeline. This interface extends the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2globalevent">ISBE2GlobalEvent</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2GlobalEvent2</b> interface inherits from <b>ISBE2GlobalEvent</b>. <b>ISBE2GlobalEvent2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2GlobalEvent2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2globalevent2-geteventex">GetEventEx</a>
</td>
<td align="left" width="63%">
Gets an global spanning event and its data from a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.



</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2GlobalEvent2)</code>.



