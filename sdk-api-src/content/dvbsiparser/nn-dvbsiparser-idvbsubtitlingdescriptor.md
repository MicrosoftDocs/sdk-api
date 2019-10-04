---
UID: NN:dvbsiparser.IDvbSubtitlingDescriptor
title: IDvbSubtitlingDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) subtitling descriptor.
old-location: mstv\idvbsubtitlingdescriptor.htm
tech.root: mstv
ms.assetid: 7308e8a9-6e16-4719-b87e-9445499f499c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbSubtitlingDescriptor, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies], IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbSubtitlingDescriptor, mstv.idvbsubtitlingdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IDvbSubtitlingDescriptor"
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
 - IDvbSubtitlingDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbSubtitlingDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) subtitling descriptor. The subtitling  descriptor  appears in the DVB service information as part of the  the program map table (PMT) and defines the language, text, and formatting that is used for subtitling data in a DVB broadcast.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbSubtitlingDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbSubtitlingDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbSubtitlingDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of subtitling records in a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getrecordancillarypageid">GetRecordAncillaryPageID</a>
</td>
<td align="left" width="63%">
Gets the ancillary page identifier for a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getrecordcompositionpageid">GetRecordCompositionPageID</a>
</td>
<td align="left" width="63%">
 Gets the composition page identifier for a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getrecordlangid">GetRecordLangId</a>
</td>
<td align="left" width="63%">
Gets the three-character ISO 639 language code for the subtitles in a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getrecordsubtitlingtype">GetRecordSubtitlingType</a>
</td>
<td align="left" width="63%">
Gets the subtitling component type from a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB subtitling descriptor.

</td>
</tr>
</table> 

