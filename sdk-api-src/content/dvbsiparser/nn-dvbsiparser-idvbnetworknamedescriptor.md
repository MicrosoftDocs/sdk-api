---
UID: NN:dvbsiparser.IDvbNetworkNameDescriptor
title: IDvbNetworkNameDescriptor
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) network name descriptor. The network name descriptor gets text format information about the network that originated the broadcast.
old-location: mstv\idvbnetworknamedescriptor.htm
old-project: mstv
ms.assetid: 1b80892d-05e6-4776-932a-a9e2bf985984
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDvbNetworkNameDescriptor, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies], IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/ IDvbNetworkNameDescriptor, mstv.idvbnetworknamedescriptor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbNetworkNameDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbNetworkNameDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) network name descriptor. The network name descriptor gets text format information about the network that originated the broadcast.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbNetworkNameDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b> IDvbNetworkNameDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbNetworkNameDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22841428-c223-4385-97c3-bd1819468866">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB network name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/261a6c65-65a5-43ed-aaed-12968b996c5a">GetNetworkName</a>
</td>
<td align="left" width="63%">
Gets the network name in ASCII text format from a DVB network name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c7e1507-2b55-468d-b83d-643a45118429">GetNetworkNameW</a>
</td>
<td align="left" width="63%">
Gets the network name in Unicode text format from a DVB network name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bc0ffea-ef18-488e-adeb-a5fd19b343a6">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB network name descriptor.

</td>
</tr>
</table> 

