---
UID: NN:dvbsiparser.IDvbShortEventDescriptor
title: IDvbShortEventDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) short event descriptor.
old-location: mstv\idvbshorteventdescriptor.htm
tech.root: mstv
ms.assetid: 039ae2e1-1dad-4a70-a054-bd95b0b500fb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbShortEventDescriptor, IDvbShortEventDescriptor interface [Microsoft TV Technologies], IDvbShortEventDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbShortEventDescriptor, mstv.idvbshorteventdescriptor
ms.topic: interface
f1_keywords: ["dvbsiparser/IDvbShortEventDescriptor"]
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
 - IDvbShortEventDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbShortEventDescriptor interface


## -description


Implements methods that get data  from a Digital Video Broadcast (DVB) short event descriptor. A short event descriptor appears as part of the DVB service information in the event information table (EIT) and service information table (SIT) and provides the name and a description of the event in text format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbShortEventDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbShortEventDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbShortEventDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbshorteventdescriptor-geteventnamew">GetEventNameW</a>
</td>
<td align="left" width="63%">
Gets the event name in Unicode string format from a DVB short event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbshorteventdescriptor-getlanguagecode">GetLanguageCode</a>
</td>
<td align="left" width="63%">
Gets the three-character ISO 639 language identifier for the DVB short event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbshorteventdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB short event descriptor

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbshorteventdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB short event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbshorteventdescriptor-gettextw">GetTextW</a>
</td>
<td align="left" width="63%">
Gets the text that describes the event in string format from a DVB short event descriptor.

</td>
</tr>
</table> 

