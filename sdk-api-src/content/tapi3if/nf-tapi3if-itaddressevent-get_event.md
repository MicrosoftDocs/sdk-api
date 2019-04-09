---
UID: NF:tapi3if.ITAddressEvent.get_Event
title: ITAddressEvent::get_Event (tapi3if.h)
author: windows-sdk-content
description: The get_Event method gets the ADDRESS_EVENT descriptor of an event.
old-location: tapi3\itaddressevent_get_event.htm
tech.root: Tapi
ms.assetid: 46dc4ce8-2453-47bb-a101-d925c9317b90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAddressEvent interface [TAPI 2.2],get_Event method, ITAddressEvent.get_Event, ITAddressEvent::get_Event, _tapi3_itaddressevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITAddressEvent interface, tapi3.itaddressevent_get_event, tapi3if/ITAddressEvent::get_Event
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
 - ITAddressEvent.get_Event
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressEvent::get_Event


## -description


The 
<b>get_Event</b> method gets the 
<a href="https://msdn.microsoft.com/7fb4acab-d60a-4848-a426-5e2960efefc1">ADDRESS_EVENT</a> descriptor of an event.


## -parameters




### -param pEvent [out]

Pointer to the 
<a href="https://msdn.microsoft.com/7fb4acab-d60a-4848-a426-5e2960efefc1">ADDRESS_EVENT</a> descriptor of an event.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



Certain events on PnP devices, such as AE_NEWTERMINAL and AE_REMOVETERMINAL, will not be received until after the first time static terminals are enumerated using 
<a href="https://msdn.microsoft.com/91fea706-9792-40e1-b812-f7578bc7968b">ITTerminalSupport::EnumerateStaticTerminals</a> or 
<a href="https://msdn.microsoft.com/f4cdd3f5-ca8c-4660-b37c-c38779a516dd">ITTerminalSupport::get_StaticTerminals</a>.




## -see-also




<a href="https://msdn.microsoft.com/7fb4acab-d60a-4848-a426-5e2960efefc1">ADDRESS_EVENT</a>



<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/340d938a-a107-4317-af65-3dca98102767">ITAddressEvent</a>
 

 

