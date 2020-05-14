---
UID: NN:dvbsiparser.IDvbDataBroadcastIDDescriptor
title: IDvbDataBroadcastIDDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) data broadcast ID descriptor.helpviewer_keywords: ["IDvbDataBroadcastIDDescriptor","IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies]","IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbDataBroadcastIDDescriptor","mstv.idvbdatabroadcastiddescriptor"]
old-location: mstv\idvbdatabroadcastiddescriptor.htm
tech.root: mstv
ms.assetid: 8d46cffc-cb49-4749-a1b7-e05d5d90941f
ms.date: 12/05/2018
ms.keywords: IDvbDataBroadcastIDDescriptor, IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies], IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbDataBroadcastIDDescriptor, mstv.idvbdatabroadcastiddescriptor
f1_keywords:
- dvbsiparser/IDvbDataBroadcastIDDescriptor
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
- IDvbDataBroadcastIDDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbDataBroadcastIDDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) data broadcast ID descriptor. The data broadcast ID descriptor is a short form of the digital broadcast descriptor that can appear in a DVB program map table (PMT) and that describes the type of a data component.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbDataBroadcastIDDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbDataBroadcastIDDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbDataBroadcastIDDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastiddescriptor-getdatabroadcastid">GetDataBroadcastID</a>
</td>
<td align="left" width="63%">
Gets the broadcast identifier from a DVB data broadcast ID descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastiddescriptor-getidselectorbytes">GetIDSelectorBytes</a>
</td>
<td align="left" width="63%">
Get the selector from a DVB data broadcast ID descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastiddescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB data broadcast ID descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastiddescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB data broadcast ID descriptor.

</td>
</tr>
</table> 

