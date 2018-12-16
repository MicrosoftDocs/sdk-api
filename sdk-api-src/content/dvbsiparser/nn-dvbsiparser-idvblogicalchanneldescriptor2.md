---
UID: NN:dvbsiparser.IDvbLogicalChannelDescriptor2
title: IDvbLogicalChannelDescriptor2
author: windows-sdk-content
description: The IDvbLogicalChannelDescriptor2 interface enables the client to get a logical channel descriptor from a DVB stream. The logical channel descriptor may be present in the network information table (NIT).
old-location: mstv\idvblogicalchanneldescriptor2.htm
tech.root: mstv
ms.assetid: 1A554897-D223-4172-B71B-ACD11BCA290A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvbLogicalChannelDescriptor2, IDvbLogicalChannelDescriptor2 interface [Microsoft TV Technologies], IDvbLogicalChannelDescriptor2 interface [Microsoft TV Technologies],described, dvbsiparser/IDvbLogicalChannelDescriptor2, mstv.idvblogicalchanneldescriptor2
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDvbLogicalChannelDescriptor2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbLogicalChannelDescriptor2 interface


## -description


The <b>IDvbLogicalChannelDescriptor2</b> interface enables the client to get a logical channel descriptor from a DVB stream. The logical channel descriptor may be present in the network information table (NIT).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbLogicalChannelDescriptor2</b> interface inherits from <a href="https://msdn.microsoft.com/6e0a99e9-088f-420c-bb60-2d324aa28227">IDvbLogicalChannelDescriptor</a>. <b>IDvbLogicalChannelDescriptor2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbLogicalChannelDescriptor2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e9d5d7f-4816-4eb8-894a-85dd7977c62e">GetListRecordLogicalChannelAndVisibility</a>
</td>
<td align="left" width="63%">
Gets a logical channel number and visibility flag  from a channel list in a logical channel descriptor.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6e0a99e9-088f-420c-bb60-2d324aa28227">IDvbLogicalChannelDescriptor</a>
 

 

