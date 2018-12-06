---
UID: NN:dvbsiparser.IDvbExtendedEventDescriptor
title: IDvbExtendedEventDescriptor
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) extended event descriptor.
old-location: mstv\idvbextendedeventdescriptor.htm
tech.root: mstv
ms.assetid: db100f17-f7b8-4252-8090-44567ab9dcbe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvbExtendedEventDescriptor, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies], IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbExtendedEventDescriptor, mstv.idvbextendedeventdescriptor
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
 - IDvbExtendedEventDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbExtendedEventDescriptor interface


## -description


Implements methods that get data  from a Digital Video Broadcast (DVB) extended event descriptor. An extended  event descriptor appears as part of the DVB service information in the event information table (EIT) and service information table (SIT). The descriptor provides a detailed text description of an event that may be used in addition to the
short event descriptor. More than one extended event descriptor can be associated to allow more than 256 bytes of information about one event
to be conveyed. Text information can be structured into two columns, one that provides an
item description field, and one that provides the item text, for example, to include a cast list in a movie or show description.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbExtendedEventDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbExtendedEventDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbExtendedEventDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b90a2de-8447-4038-9a11-1db74ebd2feb">GetConcatenatedItemW</a>
</td>
<td align="left" width="63%">
Concatenates the bytes from the item in the current DVB extended event descriptor with the bytes from the item in the next DVB extended event descriptor and returns the concatenated data as a Unicode string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8cbfe2c-db33-449d-991c-5fb50d8d974f">GetConcatenatedTextW</a>
</td>
<td align="left" width="63%">
Gets the concatenation of the text description in the current item with the text description in the next item of a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db065f1a-8354-4207-b7f7-d67adf094c70">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of item descriptions  from a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cf156fe-bfdd-444d-be4e-422c11ab08dc">GetDescriptorNumber</a>
</td>
<td align="left" width="63%">
Gets the descriptor number from a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f63b7fa9-969e-43d4-95f3-445d6265f445">GetLanguageCode</a>
</td>
<td align="left" width="63%">
Gets the ISO 639 language identifier for the DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fccfec3b-0177-4a3d-8c82-0cba3633a613">GetLastDescriptorNumber</a>
</td>
<td align="left" width="63%">
Gets the number of the last descriptor associated with this descriptor from a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5109cdff-27a0-41e5-9b9e-25a82d176e14">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed3046ad-b987-479a-a2ba-d761b2d83c86">GetRecordItemRawBytes</a>
</td>
<td align="left" width="63%">
Gets the raw data from the 
current item in a DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39c046b0-d357-44c5-9abe-2fb3998b7677">GetRecordItemW</a>
</td>
<td align="left" width="63%">
Gets the item and descriptor in Unicode string format from a  DVB extended event descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f6dad8a-fd95-48c3-9bb2-222c5ec958f5">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a Digital Video Broadcast (DVB) data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18433c81-c58f-4657-90b0-183b1ad9f8e8">GetTextW</a>
</td>
<td align="left" width="63%">
Gets the text describing the event in Unicode string format from a DVB extended event descriptor.

</td>
</tr>
</table> 

