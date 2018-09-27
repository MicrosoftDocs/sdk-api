---
UID: NN:dvbsiparser.IDVB_TDT
title: IDVB_TDT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_tdt.htm
tech.root: MSTV
ms.assetid: 15fed2d3-fcc8-4992-9dff-4cd5f617e55b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDVB_TDT, IDVB_TDT interface [Microsoft TV Technologies], IDVB_TDT interface [Microsoft TV Technologies],described, IDVB_TDTInterface, dvbsiparser/IDVB_TDT, mstv.idvb_tdt
ms.prod: windows
ms.technology: windows-sdk
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_TDT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_TDT</b> interface enables the client to get information from a time and date table (TDT). The <a href="https://msdn.microsoft.com/0922ccda-7bd8-480d-8cd1-64f170b7ec69">IDvbSiParser::GetTDT</a> method returns a pointer to this interface. The TDT provides the current time and date, in Universal Time Coordinated (UTC) format.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_TDT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_TDT</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a3c45e91-3e30-4f22-aedb-d81024160e88">GetUTCTime</a>
</td>
<td align="left" width="63%">
Returns the current UTC time and date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/265a171b-57be-40dd-9891-e8a3b64af574">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

