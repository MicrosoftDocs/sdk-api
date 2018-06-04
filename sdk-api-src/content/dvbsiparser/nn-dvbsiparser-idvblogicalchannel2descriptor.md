---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDvbLogicalChannel2Descriptor interface


## -description


Implements methods that  get data from a logical channel descriptor (LCD) in a Digital Video Broadcast (DVB) MPEG-2 stream that uses the format defined in the Nordig specification used in Scandinavian countries.

 The logical channel descriptor may be present in the network information table (NIT).

By default, all methods in the base interface <a href="https://msdn.microsoft.com/6e0a99e9-088f-420c-bb60-2d324aa28227">IDvbLogicalChannelDescriptor</a> act on the first item in a list.  Once any  call to a <b>IDvbLogicalChannel2Descriptor</b> method completes successfully, the item that the method returns remains selected so that subsequent calls to <b>IDvbLogicalChannelDescriptor</b> methods act on the selected item.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbLogicalChannel2Descriptor</b> interface inherits from <a href="https://msdn.microsoft.com/6e0a99e9-088f-420c-bb60-2d324aa28227">IDvbLogicalChannelDescriptor2</a>. <b>IDvbLogicalChannel2Descriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbLogicalChannel2Descriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13a439d1-c6b6-49ab-a41e-caa27e320f37">GetCountOfLists</a>
</td>
<td align="left" width="63%">
Gets the number of channel lists from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">GetListCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in a channel list from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42f3c684-64c3-4bcb-b9c0-25a008075902">GetListCountryCode</a>
</td>
<td align="left" width="63%">
Gets the country code for a channel list from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39f97d38-d588-43d0-8aea-6ef4e1b3440b">GetListId</a>
</td>
<td align="left" width="63%">
Gets a channel list identifier from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbfee1d5-8a38-4c9a-ae5e-2d91970c132e">GetListNameW</a>
</td>
<td align="left" width="63%">
Gets a country list name  from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8ebc804-08a1-4840-ba20-f52438a0d6bf">GetListRecordLogicalChannelNumber</a>
</td>
<td align="left" width="63%">
Gets a logical channel number from a channel list in a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebd81791-558d-4380-af4c-d8380f404771">GetListRecordServiceId</a>
</td>
<td align="left" width="63%">
Gets a service identifier from a logical channel descriptor.

</td>
</tr>
</table> 

