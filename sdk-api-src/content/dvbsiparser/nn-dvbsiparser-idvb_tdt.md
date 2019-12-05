---
UID: NN:dvbsiparser.IDVB_TDT
title: IDVB_TDT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_tdt.htm
tech.root: mstv
ms.assetid: 15fed2d3-fcc8-4992-9dff-4cd5f617e55b
ms.date: 12/05/2018
ms.keywords: IDVB_TDT, IDVB_TDT interface [Microsoft TV Technologies], IDVB_TDT interface [Microsoft TV Technologies],described, IDVB_TDTInterface, dvbsiparser/IDVB_TDT, mstv.idvb_tdt
ms.topic: interface
f1_keywords:
- dvbsiparser/IDVB_TDT
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- IDVB_TDT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_TDT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_TDT</b> interface enables the client to get information from a time and date table (TDT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-gettdt">IDvbSiParser::GetTDT</a> method returns a pointer to this interface. The TDT provides the current time and date, in Universal Time Coordinated (UTC) format.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_TDT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_TDT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_TDT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_tdt-getutctime">GetUTCTime</a>
</td>
<td align="left" width="63%">
Returns the current UTC time and date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_tdt-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

