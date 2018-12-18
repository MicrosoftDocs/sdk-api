---
UID: NN:dvbsiparser.IDvbTeletextDescriptor
title: IDvbTeletextDescriptor
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) teletext descriptor. The teletext descriptor is the part of the DVB program map table (PMT) that identifies European Broadcasting Union (EBU) teletext streams.
old-location: mstv\idvbteletextdescriptor.htm
tech.root: mstv
ms.assetid: 5148a87b-e6b6-4bda-871c-10a2f398ebcc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvbTeletextDescriptor, IDvbTeletextDescriptor interface [Microsoft TV Technologies], IDvbTeletextDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbTeletextDescriptor, mstv.idvbteletextdescriptor
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
 - IDvbTeletextDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbTeletextDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) teletext descriptor. 
The teletext descriptor is the part of the DVB program map table (PMT) that identifies European Broadcasting Union 
(EBU) teletext streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbTeletextDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbTeletextDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service records in a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e785d05a-d4f1-40d8-b93e-ea944373f4c3">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cce0fd15-5098-4871-baab-e40b6cae39b1">GetRecordLangId</a>
</td>
<td align="left" width="63%">
Gets the three-character ISO 639 language code from a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb3c39b6-dc85-42ca-9d4b-ad27eae077dd">GetRecordMagazineNumber</a>
</td>
<td align="left" width="63%">
Gets the magazine number from a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/323af443-8ef3-443e-9d6c-7af17419655a">GetRecordPageNumber</a>
</td>
<td align="left" width="63%">
Gets the page number from a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4272d95a-406f-4afc-92b9-abfd618f41ab">GetRecordTeletextType</a>
</td>
<td align="left" width="63%">
Gets the teletext type code from a DVB teletext descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f359c37-8d8f-48de-a4a2-89617c5761ed">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that idenfities a DVB teletext descriptor.

</td>
</tr>
</table> 

