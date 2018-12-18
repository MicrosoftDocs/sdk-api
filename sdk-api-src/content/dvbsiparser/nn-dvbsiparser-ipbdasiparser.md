---
UID: NN:dvbsiparser.IPBDASiParser
title: IPBDASiParser
author: windows-sdk-content
description: Implements methods that retrieve program and system information protocol (PSIP) and service information (SI) tables from a Protected Broadcast Driver Architecture (PBDA) transport stream.
old-location: mstv\ipbdasiparser.htm
tech.root: mstv
ms.assetid: a1cc25ec-b519-4c24-ba85-f2c240749fbd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPBDASiParser, IPBDASiParser interface [DirectShow], IPBDASiParser interface [DirectShow],described, dvbsiparser/IPBDASiParser, mstv.ipbdasiparser
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPBDASiParser interface


## -description


Implements methods that retrieve program and system information protocol (PSIP) and service information (SI) tables from a Protected Broadcast Driver Architecture (PBDA) transport stream.

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDASiParser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPBDASiParser</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ab7df40a-6a1c-4017-bece-618fb75797cf">GetEIT</a>
</td>
<td align="left" width="63%">
Retrieves the event information table (EIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d6848f2-6fcd-4e7c-b1fc-b8f56e6c65b6">GetServices</a>
</td>
<td align="left" width="63%">
Retrieves services from the IPBDA PSIP parser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb161e1a-ae10-4d5e-907a-91c7e80c11d8">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the IPBDA PSIP parser.

</td>
</tr>
</table> 

