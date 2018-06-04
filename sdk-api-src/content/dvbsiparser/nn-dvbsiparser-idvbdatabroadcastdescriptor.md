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

# IDvbDataBroadcastDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) data broadcast descriptor. 
 The data broadcast  descriptor  appears in the DVB service information as part of the  service description table (SDT) or event information table (EIT) and identifies the type of the data component.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbDataBroadcastDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbDataBroadcastDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbDataBroadcastDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b4c93ff-063b-4ebb-bc9a-09ec9cb6d538">GetComponentTag</a>
</td>
<td align="left" width="63%">
Gets the component tag from a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0124e197-85a0-47bf-afb6-100c344e9c9e">GetDataBroadcastID</a>
</td>
<td align="left" width="63%">
Gets the broadcast identifier from a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56fc47d6-042e-48ad-a0b8-39646453a6af">GetLangID</a>
</td>
<td align="left" width="63%">
Gets the ISO 639 language identifier for the text description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/426292bf-0cc3-4494-bd9a-b63229671bfb">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72fca5a8-2ea5-4000-8b00-dbd408cba602">GetSelectorBytes</a>
</td>
<td align="left" width="63%">
Get the selector from a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc1d25be-6f33-4281-a75c-74c7331ab6ed">GetSelectorLength</a>
</td>
<td align="left" width="63%">
Gets the length of the selector in a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f49a4c3-8e40-4cb2-ba3c-ef0b945243f9">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>
</td>
<td align="left" width="63%">
Gets the text description from a DVB data broadcast descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ae91ff-d984-4955-aa1c-d166fb491d79">GetTextLength</a>
</td>
<td align="left" width="63%">
Gets the length of the text description from a DVB data broadcast descriptor.

</td>
</tr>
</table> 

