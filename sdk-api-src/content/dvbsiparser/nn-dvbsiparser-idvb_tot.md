---
UID: NN:dvbsiparser.IDVB_TOT
title: IDVB_TOT
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_tot.htm
old-project: mstv
ms.assetid: fe5b6b7c-fc6b-4889-b780-4b9f61f3e895
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDVB_TOT, IDVB_TOT interface [Microsoft TV Technologies], IDVB_TOT interface [Microsoft TV Technologies], described, IDVB_TOTInterface, dvbsiparser/IDVB_TOT, mstv.idvb_tot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDVB_TOT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_TOT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_TOT</b> interface enables the client to get information from a time offset table (TOT). The <a href="https://msdn.microsoft.com/07e27472-2cb9-4bb1-9976-200bcdccb539">IDvbSiParser::GetTOT</a> method returns a pointer to this information. A TOT contains the current UTC time, plus the offset from UTC for local time in one or more regions. The offsets are contained in a <i>local offset time descriptor</i>, as specified by ETSI EN 300 468.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_TOT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_TOT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_TOT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c043aa8-683b-4770-81cb-3d3e9c35342f">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors in the TOT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d59b778-c8bc-4ccc-bca2-013c2345814f">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for the TOT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64830b54-f89d-44cc-9b05-e188b8f28f55">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the TOT for a descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67092908-b2bb-4dc6-8fb4-d45b03823c69">GetUTCTime</a>
</td>
<td align="left" width="63%">
Returns the current UTC time and date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

