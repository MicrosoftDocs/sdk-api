---
UID: NN:tapi3if.ITAddressDeviceSpecificEvent
title: ITAddressDeviceSpecificEvent
author: windows-sdk-content
description: The ITAddressDeviceSpecificEvent exposes methods that allow an application to retrieve information about a device-specific event.
old-location: tapi3\itaddressdevicespecificevent.htm
old-project: tapi
ms.assetid: 8590e9b1-2bbf-47e5-96de-8765a475a972
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITAddressDeviceSpecificEvent, ITAddressDeviceSpecificEvent interface [TAPI 2.2], ITAddressDeviceSpecificEvent interface [TAPI 2.2],described, _tapi3_itaddressdevicespecificevent, tapi3.itaddressdevicespecificevent, tapi3if/ITAddressDeviceSpecificEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressDeviceSpecificEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddressDeviceSpecificEvent interface


## -description


The 
<b>ITAddressDeviceSpecificEvent</b> exposes methods that allow an application to retrieve information about a device-specific event.

For a code example that illustrates how to create this interface, see the 
<a href="https://msdn.microsoft.com/236d4e7f-865f-4b26-8da6-c86476588c47">Phone and Address Device-specific Events</a> topic.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddressDeviceSpecificEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITAddressDeviceSpecificEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAddressDeviceSpecificEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95b745c9-c18a-47c9-8ceb-b2c225ebbf73">get_Address</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface of the Address object involved in the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcf3b82d-5c1f-41f7-bb6a-6470a96f4049">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface of the Call object involved in the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0cae67a-0c39-407a-b563-bef14c36f014">get_lParam1</a>
</td>
<td align="left" width="63%">
Gets the first device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b155cf6b-babd-4c47-8571-96f970878d81">get_lParam2</a>
</td>
<td align="left" width="63%">
Gets the second device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e0a513d-2bf4-4bdf-926f-2e88a8465073">get_lParam3</a>
</td>
<td align="left" width="63%">
Gets the third device-specific buffer.

</td>
</tr>
</table> 

