---
UID: NN:dvbsiparser.IDvbSubtitlingDescriptor
title: IDvbSubtitlingDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) subtitling descriptor.
old-location: mstv\idvbsubtitlingdescriptor.htm
tech.root: mstv
ms.assetid: 7308e8a9-6e16-4719-b87e-9445499f499c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvbSubtitlingDescriptor, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies], IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbSubtitlingDescriptor, mstv.idvbsubtitlingdescriptor
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
 - IDvbSubtitlingDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbSubtitlingDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) subtitling descriptor. The subtitling  descriptor  appears in the DVB service information as part of the  the program map table (PMT) and defines the language, text, and formatting that is used for subtitling data in a DVB broadcast.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbSubtitlingDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbSubtitlingDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8cc25b63-de43-4f8d-af19-c3bb8c389a55">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of subtitling records in a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b02c37c-4411-4d69-af5d-d758b18fe42c">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab490087-063d-4e9f-8aa5-679804548d26">GetRecordAncillaryPageID</a>
</td>
<td align="left" width="63%">
Gets the ancillary page identifier for a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/108f431a-e3c3-42d5-ad27-b7a54029051f">GetRecordCompositionPageID</a>
</td>
<td align="left" width="63%">
 Gets the composition page identifier for a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03a6a71f-ccec-4e4f-a24c-2ac81dd1a0ba">GetRecordLangId</a>
</td>
<td align="left" width="63%">
Gets the three-character ISO 639 language code for the subtitles in a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ab91508-9afe-4ab7-957f-5467e87ce7ee">GetRecordSubtitlingType</a>
</td>
<td align="left" width="63%">
Gets the subtitling component type from a DVB subtitling descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b16b66d-5e71-4204-984d-e9a9d677f4a9">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB subtitling descriptor.

</td>
</tr>
</table> 

