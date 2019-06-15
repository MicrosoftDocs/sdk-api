---
UID: NN:dvbsiparser.IDvbTeletextDescriptor
title: IDvbTeletextDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) teletext descriptor. The teletext descriptor is the part of the DVB program map table (PMT) that identifies European Broadcasting Union (EBU) teletext streams.
old-location: mstv\idvbteletextdescriptor.htm
tech.root: mstv
ms.assetid: 5148a87b-e6b6-4bda-871c-10a2f398ebcc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbTeletextDescriptor, IDvbTeletextDescriptor interface [Microsoft TV Technologies], IDvbTeletextDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbTeletextDescriptor, mstv.idvbteletextdescriptor
ms.topic: interface
f1_keywords: ["dvbsiparser/IDvbTeletextDescriptor"]
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
 - IDvbTeletextDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbTeletextDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) teletext descriptor. 
The teletext descriptor is the part of the DVB program map table (PMT) that identifies European Broadcasting Union 
(EBU) teletext streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbTeletextDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbTeletextDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbTeletextDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service records in a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getrecordlangid">GetRecordLangId</a>
</td>
<td align="left" width="63%">
Gets the three-character ISO 639 language code from a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getrecordmagazinenumber">GetRecordMagazineNumber</a>
</td>
<td align="left" width="63%">
Gets the magazine number from a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getrecordpagenumber">GetRecordPageNumber</a>
</td>
<td align="left" width="63%">
Gets the page number from a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getrecordteletexttype">GetRecordTeletextType</a>
</td>
<td align="left" width="63%">
Gets the teletext type code from a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that idenfities a DVB teletext descriptor.

</td>
</tr>
</table> 

