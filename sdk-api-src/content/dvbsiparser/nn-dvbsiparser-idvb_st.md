---
UID: NN:dvbsiparser.IDVB_ST
title: IDVB_ST
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_st.htm
tech.root: MSTV
ms.assetid: 56d77564-4de3-4252-9218-a1188f363437
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDVB_ST, IDVB_ST interface [Microsoft TV Technologies], IDVB_ST interface [Microsoft TV Technologies],described, IDVB_STInterface, dvbsiparser/IDVB_ST, mstv.idvb_st
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
 - IDVB_ST
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_ST interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_ST</b> interface enables the client to get information from a stuffing table (ST). The <a href="https://msdn.microsoft.com/417f7651-dd6f-4399-8a32-d1b7505efb71">IDvbSiParser::GetST</a> method returns a pointer to this interface.

The purpose of an ST is to invalidate existing table sections when the transport stream crosses the boundary between delivery systems. To invalidate a table section, the section is overwritten with an ST.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_ST</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_ST</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3afdafad-462c-4fad-a9c6-ec820bedf31a">GetData</a>
</td>
<td align="left" width="63%">
Returns the data in the ST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d42f147-b82d-4236-9e58-c42019d6b413">GetDataLength</a>
</td>
<td align="left" width="63%">
Returns the length of the data in the ST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eda69656-9e66-4366-84fe-e8ffecc93fc3">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

