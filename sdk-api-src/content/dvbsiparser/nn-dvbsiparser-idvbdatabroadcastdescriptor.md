---
UID: NN:dvbsiparser.IDvbDataBroadcastDescriptor
title: IDvbDataBroadcastDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) data broadcast descriptor.
helpviewer_keywords: ["IDvbDataBroadcastDescriptor","IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies]","IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbDataBroadcastDescriptor","mstv.idvbdatabroadcastdescriptor"]
old-location: mstv\idvbdatabroadcastdescriptor.htm
tech.root: mstv
ms.assetid: 3b1d2711-e5ad-4d4c-bc8f-e199bcd75799
ms.date: 12/05/2018
ms.keywords: IDvbDataBroadcastDescriptor, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies], IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbDataBroadcastDescriptor, mstv.idvbdatabroadcastdescriptor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbDataBroadcastDescriptor
 - dvbsiparser/IDvbDataBroadcastDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbDataBroadcastDescriptor
---

# IDvbDataBroadcastDescriptor interface


## -description

Implements methods that get data from a Digital Video Broadcast (DVB) data broadcast descriptor. 
 The data broadcast  descriptor  appears in the DVB service information as part of the  service description table (SDT) or event information table (EIT) and identifies the type of the data component.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbDataBroadcastDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbDataBroadcastDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbDataBroadcastDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-getcomponenttag">GetComponentTag</a>
</td>
<td align="left" width="63%">
Gets the component tag from a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-getdatabroadcastid">GetDataBroadcastID</a>
</td>
<td align="left" width="63%">
Gets the broadcast identifier from a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-getlangid">GetLangID</a>
</td>
<td align="left" width="63%">
Gets the ISO 639 language identifier for the text description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-getselectorbytes">GetSelectorBytes</a>
</td>
<td align="left" width="63%">
Get the selector from a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-getselectorlength">GetSelectorLength</a>
</td>
<td align="left" width="63%">
Gets the length of the selector in a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-gettext">GetText</a>
</td>
<td align="left" width="63%">
Gets the text description from a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdatabroadcastdescriptor-gettextlength">GetTextLength</a>
</td>
<td align="left" width="63%">
Gets the length of the text description from a DVB data broadcast descriptor.

</td>
</tr>
</table>