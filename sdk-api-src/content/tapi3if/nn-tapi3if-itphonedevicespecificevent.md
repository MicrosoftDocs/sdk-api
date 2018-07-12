---
UID: NN:tapi3if.ITPhoneDeviceSpecificEvent
title: ITPhoneDeviceSpecificEvent
author: windows-sdk-content
description: The ITPhoneDeviceSpecificEvent exposes methods that allow an application to retrieve information about a phone device-specific event.
old-location: tapi3\itphonedevicespecificevent.htm
old-project: tapi
ms.assetid: a4b2fb49-6128-41b6-8eb3-13a8bbba66ac
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITPhoneDeviceSpecificEvent, ITPhoneDeviceSpecificEvent interface [TAPI 2.2], ITPhoneDeviceSpecificEvent interface [TAPI 2.2],described, _tapi3_itphonedevicespecificevent, tapi3.itphonedevicespecificevent, tapi3if/ITPhoneDeviceSpecificEvent
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
 - ITPhoneDeviceSpecificEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhoneDeviceSpecificEvent interface


## -description


The 
<b>ITPhoneDeviceSpecificEvent</b> exposes methods that allow an application to retrieve information about a phone device-specific event.

For a code example that illustrates how to create this interface, see the 
<a href="https://msdn.microsoft.com/236d4e7f-865f-4b26-8da6-c86476588c47">Phone and Address Device-specific Events</a> topic.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPhoneDeviceSpecificEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITPhoneDeviceSpecificEvent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fc75bbfa-7b0b-4ecc-99cc-48517550d71d">get_lParam1</a>
</td>
<td align="left" width="63%">
Gets the first device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58784ca2-ca2e-4a89-9b8c-3a6118b0ef2d">get_lParam2</a>
</td>
<td align="left" width="63%">
Gets the second device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dd4c5d7-033a-4e25-a7f0-6731b5b08d18">get_lParam3</a>
</td>
<td align="left" width="63%">
Gets the third device-specific buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/068f4172-92a4-41cc-b554-c6e4014505eb">get_Phone</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface pointer for a phone device event.

</td>
</tr>
</table> 

