---
UID: NN:dvbsiparser.IDVB_ST
title: IDVB_ST (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_st.htm
tech.root: mstv
ms.assetid: 56d77564-4de3-4252-9218-a1188f363437
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVB_ST, IDVB_ST interface [Microsoft TV Technologies], IDVB_ST interface [Microsoft TV Technologies],described, IDVB_STInterface, dvbsiparser/IDVB_ST, mstv.idvb_st
ms.topic: interface
f1_keywords: ["dvbsiparser/IDVB_ST"]
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
 - IDVB_ST
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_ST interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_ST</b> interface enables the client to get information from a stuffing table (ST). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getst">IDvbSiParser::GetST</a> method returns a pointer to this interface.

The purpose of an ST is to invalidate existing table sections when the transport stream crosses the boundary between delivery systems. To invalidate a table section, the section is overwritten with an ST.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_ST</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_ST</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_ST</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_st-getdata">GetData</a>
</td>
<td align="left" width="63%">
Returns the data in the ST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_st-getdatalength">GetDataLength</a>
</td>
<td align="left" width="63%">
Returns the length of the data in the ST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_st-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

