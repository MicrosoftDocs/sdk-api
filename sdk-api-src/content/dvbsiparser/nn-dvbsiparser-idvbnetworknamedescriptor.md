---
UID: NN:dvbsiparser.IDvbNetworkNameDescriptor
title: IDvbNetworkNameDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) network name descriptor. The network name descriptor gets text format information about the network that originated the broadcast.
old-location: mstv\idvbnetworknamedescriptor.htm
tech.root: mstv
ms.assetid: 1b80892d-05e6-4776-932a-a9e2bf985984
ms.date: 12/05/2018
ms.keywords: IDvbNetworkNameDescriptor, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies], IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/ IDvbNetworkNameDescriptor, mstv.idvbnetworknamedescriptor
f1_keywords:
- dvbsiparser/IDvbNetworkNameDescriptor
dev_langs:
- c++
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
- IDvbNetworkNameDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbNetworkNameDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) network name descriptor. The network name descriptor gets text format information about the network that originated the broadcast.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbNetworkNameDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b> IDvbNetworkNameDescriptor</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbnetworknamedescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB network name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbnetworknamedescriptor-getnetworkname">GetNetworkName</a>
</td>
<td align="left" width="63%">
Gets the network name in ASCII text format from a DVB network name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbnetworknamedescriptor-getnetworknamew">GetNetworkNameW</a>
</td>
<td align="left" width="63%">
Gets the network name in Unicode text format from a DVB network name descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbnetworknamedescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB network name descriptor.

</td>
</tr>
</table> 

