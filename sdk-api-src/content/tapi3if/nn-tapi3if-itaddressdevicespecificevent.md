---
UID: NN:tapi3if.ITAddressDeviceSpecificEvent
title: ITAddressDeviceSpecificEvent (tapi3if.h)
author: windows-sdk-content
description: The ITAddressDeviceSpecificEvent exposes methods that allow an application to retrieve information about a device-specific event.
old-location: tapi3\itaddressdevicespecificevent.htm
tech.root: Tapi
ms.assetid: 8590e9b1-2bbf-47e5-96de-8765a475a972
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAddressDeviceSpecificEvent, ITAddressDeviceSpecificEvent interface [TAPI 2.2], ITAddressDeviceSpecificEvent interface [TAPI 2.2],described, _tapi3_itaddressdevicespecificevent, tapi3.itaddressdevicespecificevent, tapi3if/ITAddressDeviceSpecificEvent
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITAddressDeviceSpecificEvent"
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddressDeviceSpecificEvent interface


## -description


The 
<b>ITAddressDeviceSpecificEvent</b> exposes methods that allow an application to retrieve information about a device-specific event.

For a code example that illustrates how to create this interface, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/phone-and-address-device-specific-events">Phone and Address Device-specific Events</a> topic.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddressDeviceSpecificEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddressDeviceSpecificEvent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddressdevicespecificevent-get_address">get_Address</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface of the Address object involved in the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddressdevicespecificevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface of the Call object involved in the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddressdevicespecificevent-get_lparam1">get_lParam1</a>
</td>
<td align="left" width="63%">
Gets the first device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddressdevicespecificevent-get_lparam2">get_lParam2</a>
</td>
<td align="left" width="63%">
Gets the second device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddressdevicespecificevent-get_lparam3">get_lParam3</a>
</td>
<td align="left" width="63%">
Gets the third device-specific buffer.

</td>
</tr>
</table> 

