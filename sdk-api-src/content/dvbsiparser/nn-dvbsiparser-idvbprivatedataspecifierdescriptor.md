---
UID: NN:dvbsiparser.IDvbPrivateDataSpecifierDescriptor
title: IDvbPrivateDataSpecifierDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) private data descriptor. The private data descriptor describes broadcaster-specific data that is not part of the official MPEG-2 standard for broadcast streams.
helpviewer_keywords: ["IDvbPrivateDataSpecifierDescriptor","IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies]","IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbPrivateDataSpecifierDescriptor","mstv.idvbprivatedataspecifierdescriptor"]
old-location: mstv\idvbprivatedataspecifierdescriptor.htm
tech.root: mstv
ms.assetid: 0d5a78a3-0d56-47e8-939f-006d5f4db5c4
ms.date: 12/05/2018
ms.keywords: IDvbPrivateDataSpecifierDescriptor, IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies], IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbPrivateDataSpecifierDescriptor, mstv.idvbprivatedataspecifierdescriptor
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
 - IDvbPrivateDataSpecifierDescriptor
 - dvbsiparser/IDvbPrivateDataSpecifierDescriptor
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
 - IDvbPrivateDataSpecifierDescriptor
---

# IDvbPrivateDataSpecifierDescriptor interface


## -description

Implements methods that get data from a Digital Video Broadcast (DVB) private data descriptor. The private data descriptor describes broadcaster-specific data that is not part of the official MPEG-2 standard for broadcast streams.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbPrivateDataSpecifierDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbPrivateDataSpecifierDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbPrivateDataSpecifierDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbprivatedataspecifierdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB private data descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbprivatedataspecifierdescriptor-getprivatedataspecifier">GetPrivateDataSpecifier</a>
</td>
<td align="left" width="63%">
Gets data from a DVB private data descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbprivatedataspecifierdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB private data descriptor.

</td>
</tr>
</table>

