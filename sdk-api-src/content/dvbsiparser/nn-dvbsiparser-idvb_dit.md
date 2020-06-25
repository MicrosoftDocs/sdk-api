---
UID: NN:dvbsiparser.IDVB_DIT
title: IDVB_DIT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_DIT","IDVB_DIT interface [Microsoft TV Technologies]","IDVB_DIT interface [Microsoft TV Technologies]","described","IDVB_DITInterface","dvbsiparser/IDVB_DIT","mstv.idvb_dit"]
old-location: mstv\idvb_dit.htm
tech.root: mstv
ms.assetid: 8acbb1ac-100f-47b9-b8db-580d1a845946
ms.date: 12/05/2018
ms.keywords: IDVB_DIT, IDVB_DIT interface [Microsoft TV Technologies], IDVB_DIT interface [Microsoft TV Technologies],described, IDVB_DITInterface, dvbsiparser/IDVB_DIT, mstv.idvb_dit
f1_keywords:
- dvbsiparser/IDVB_DIT
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
- IDVB_DIT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_DIT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_DIT</b> interface enables the client to get information from a discontinuity information table (DIT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getdit">IDvbSiParser::GetDIT</a> method returns a pointer to this interface. The presence of a DIT in the stream indicates a transition point where the Service Information (SI) may be discontinuous.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_DIT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_DIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_DIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_dit-gettransitionflag">GetTransitionFlag</a>
</td>
<td align="left" width="63%">
Queries whether the transition_flag bit is set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_dit-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

