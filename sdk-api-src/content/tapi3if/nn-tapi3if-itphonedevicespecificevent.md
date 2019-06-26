---
UID: NN:tapi3if.ITPhoneDeviceSpecificEvent
title: ITPhoneDeviceSpecificEvent (tapi3if.h)
author: windows-sdk-content
description: The ITPhoneDeviceSpecificEvent exposes methods that allow an application to retrieve information about a phone device-specific event.
old-location: tapi3\itphonedevicespecificevent.htm
tech.root: Tapi
ms.assetid: a4b2fb49-6128-41b6-8eb3-13a8bbba66ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPhoneDeviceSpecificEvent, ITPhoneDeviceSpecificEvent interface [TAPI 2.2], ITPhoneDeviceSpecificEvent interface [TAPI 2.2],described, _tapi3_itphonedevicespecificevent, tapi3.itphonedevicespecificevent, tapi3if/ITPhoneDeviceSpecificEvent
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITPhoneDeviceSpecificEvent"
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
 - ITPhoneDeviceSpecificEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhoneDeviceSpecificEvent interface


## -description


The 
<b>ITPhoneDeviceSpecificEvent</b> exposes methods that allow an application to retrieve information about a phone device-specific event.

For a code example that illustrates how to create this interface, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/phone-and-address-device-specific-events">Phone and Address Device-specific Events</a> topic.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPhoneDeviceSpecificEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPhoneDeviceSpecificEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPhoneDeviceSpecificEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphonedevicespecificevent-get_lparam1">get_lParam1</a>
</td>
<td align="left" width="63%">
Gets the first device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphonedevicespecificevent-get_lparam2">get_lParam2</a>
</td>
<td align="left" width="63%">
Gets the second device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphonedevicespecificevent-get_lparam3">get_lParam3</a>
</td>
<td align="left" width="63%">
Gets the third device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphonedevicespecificevent-get_phone">get_Phone</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface pointer for a phone device event.

</td>
</tr>
</table> 

