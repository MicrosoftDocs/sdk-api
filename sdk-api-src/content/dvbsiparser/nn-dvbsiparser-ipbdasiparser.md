---
UID: NN:dvbsiparser.IPBDASiParser
title: IPBDASiParser (dvbsiparser.h)
description: Implements methods that retrieve program and system information protocol (PSIP) and service information (SI) tables from a Protected Broadcast Driver Architecture (PBDA) transport stream.
old-location: mstv\ipbdasiparser.htm
tech.root: mstv
ms.assetid: a1cc25ec-b519-4c24-ba85-f2c240749fbd
ms.date: 12/05/2018
ms.keywords: IPBDASiParser, IPBDASiParser interface [DirectShow], IPBDASiParser interface [DirectShow],described, dvbsiparser/IPBDASiParser, mstv.ipbdasiparser
f1_keywords:
- dvbsiparser/IPBDASiParser
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
- dvbsiparser.h
api_name:
- IPBDASiParser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDASiParser interface


## -description


Implements methods that retrieve program and system information protocol (PSIP) and service information (SI) tables from a Protected Broadcast Driver Architecture (PBDA) transport stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDASiParser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPBDASiParser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPBDASiParser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdasiparser-geteit">GetEIT</a>
</td>
<td align="left" width="63%">
Retrieves the event information table (EIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdasiparser-getservices">GetServices</a>
</td>
<td align="left" width="63%">
Retrieves services from the IPBDA PSIP parser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdasiparser-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the IPBDA PSIP parser.

</td>
</tr>
</table> 

