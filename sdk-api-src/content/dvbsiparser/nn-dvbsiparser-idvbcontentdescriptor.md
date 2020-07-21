---
UID: NN:dvbsiparser.IDvbContentDescriptor
title: IDvbContentDescriptor (dvbsiparser.h)
description: Implements methods that get information from a Digital Video Broadcast (DVB) content descriptor.
helpviewer_keywords: ["IDvbContentDescriptor","IDvbContentDescriptor interface [Microsoft TV Technologies]","IDvbContentDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbContentDescriptor","mstv.idvbcontentdescriptor"]
old-location: mstv\idvbcontentdescriptor.htm
tech.root: mstv
ms.assetid: 7bc74428-f8e3-4d3b-b35a-33e917b18a93
ms.date: 12/05/2018
ms.keywords: IDvbContentDescriptor, IDvbContentDescriptor interface [Microsoft TV Technologies], IDvbContentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbContentDescriptor, mstv.idvbcontentdescriptor
f1_keywords:
- dvbsiparser/IDvbContentDescriptor
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
- IDvbContentDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbContentDescriptor interface


## -description


Implements methods that get information from a Digital Video Broadcast (DVB) content descriptor.  Content descriptors appear in the DVB Service Information as part of the Event Information Table (EIT), which provides information about the events in each service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbContentDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbContentDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbContentDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of content elements within the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the length of the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getrecordcontentnibbles">GetRecordContentNibbles</a>
</td>
<td align="left" width="63%">
Gets the two 4-bit fields that make up a DVB-defined identifier for a content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getrecordusernibbles">GetRecordUserNibbles</a>
</td>
<td align="left" width="63%">
Gets the two 4-bit fields that make up a broadcaster-defined identifier for a content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies the descriptor.

</td>
</tr>
</table> 

