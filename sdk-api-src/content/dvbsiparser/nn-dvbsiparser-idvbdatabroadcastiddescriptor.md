---
UID: NN:dvbsiparser.IDvbDataBroadcastIDDescriptor
title: IDvbDataBroadcastIDDescriptor
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) data broadcast ID descriptor.
old-location: mstv\idvbdatabroadcastiddescriptor.htm
tech.root: mstv
ms.assetid: 8d46cffc-cb49-4749-a1b7-e05d5d90941f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvbDataBroadcastIDDescriptor, IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies], IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbDataBroadcastIDDescriptor, mstv.idvbdatabroadcastiddescriptor
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
 - IDvbDataBroadcastIDDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbDataBroadcastIDDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) data broadcast ID descriptor. The data broadcast ID descriptor is a short form of the digital broadcast descriptor that can appear in a DVB program map table (PMT) and that describes the type of a data component.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbDataBroadcastIDDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbDataBroadcastIDDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbDataBroadcastIDDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2addfb2b-80ab-47a7-81dd-f660e5fe1138">GetDataBroadcastID</a>
</td>
<td align="left" width="63%">
Gets the broadcast identifier from a DVB data broadcast ID descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b41614d6-61e4-4548-9c15-63ef100d2ab8">GetIDSelectorBytes</a>
</td>
<td align="left" width="63%">
Get the selector from a DVB data broadcast ID descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9727783-a876-40b4-b4fa-e839ef0f6502">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB data broadcast ID descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c3c13f0-03b0-47fe-bd87-5bb6d32ef838">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB data broadcast ID descriptor.

</td>
</tr>
</table> 

