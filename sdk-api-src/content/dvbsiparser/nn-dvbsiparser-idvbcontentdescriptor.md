---
UID: NN:dvbsiparser.IDvbContentDescriptor
title: IDvbContentDescriptor
author: windows-sdk-content
description: Implements methods that get information from a Digital Video Broadcast (DVB) content descriptor.
old-location: mstv\idvbcontentdescriptor.htm
tech.root: mstv
ms.assetid: 7bc74428-f8e3-4d3b-b35a-33e917b18a93
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDvbContentDescriptor, IDvbContentDescriptor interface [Microsoft TV Technologies], IDvbContentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbContentDescriptor, mstv.idvbcontentdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDvbContentDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbContentDescriptor interface


## -description


Implements methods that get information from a Digital Video Broadcast (DVB) content descriptor.  Content descriptors appear in the DVB Service Information as part of the Event Information Table (EIT), which provides information about the events in each service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbContentDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbContentDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0d4d81b3-d6d8-416b-af6b-2b6ef12cf1d9">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of content elements within the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e937c51-e143-4b13-a16a-279bd3690feb">GetLength</a>
</td>
<td align="left" width="63%">
Gets the length of the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b05403a-cf9e-4f23-907f-ffb90b6fc5e3">GetRecordContentNibbles</a>
</td>
<td align="left" width="63%">
Gets the two 4-bit fields that make up a DVB-defined identifier for a content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a071e725-c98d-4061-bda5-d7eca8b4b0e0">GetRecordUserNibbles</a>
</td>
<td align="left" width="63%">
Gets the two 4-bit fields that make up a broadcaster-defined identifier for a content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cfbda01-ef69-4b69-90f4-04dd3044ae1f">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies the descriptor.

</td>
</tr>
</table> 

