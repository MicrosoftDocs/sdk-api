---
UID: NN:tapi3if.ITTAPIObjectEvent2
title: ITTAPIObjectEvent2
author: windows-sdk-content
description: The ITTAPIObjectEvent2 interface is an extension of the ITTAPIObjectEvent interface. ITTAPIObjectEvent2 exposes an additional method that returns a pointer to an ITPhone interface on the phone object that caused the TAPI object event.
old-location: tapi3\ittapiobjectevent2.htm
old-project: Tapi
ms.assetid: ad4fc838-5a6c-4942-b5a0-ed00cea11ba8
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITTAPIObjectEvent2, ITTAPIObjectEvent2 interface [TAPI 2.2], ITTAPIObjectEvent2 interface [TAPI 2.2],described, _tapi3_ittapiobjectevent2, tapi3.ittapiobjectevent2, tapi3if/ITTAPIObjectEvent2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITTAPIObjectEvent2
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPIObjectEvent2 interface


## -description


The 
<b>ITTAPIObjectEvent2</b> interface is an extension of the 
<a href="https://msdn.microsoft.com/73be7109-0d3a-4ac5-adb7-e1577d8640b5">ITTAPIObjectEvent</a> interface. 
<b>ITTAPIObjectEvent2</b> exposes an additional method that returns a pointer to an 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface on the phone object that caused the TAPI object event.

When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_TAPIOBJECT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITTAPIObjectEvent2</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_TAPIOBJECT</b> event to enable reception of TAPI object events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPIObjectEvent2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTAPIObjectEvent2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTAPIObjectEvent2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76e316f6-536b-4531-a4a6-397e258678cc">get_Phone</a>
</td>
<td align="left" width="63%">
Returns a pointer to the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface on the phone object that caused this notification of a TAPI object event.

</td>
</tr>
</table> 


## -see-also




<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://msdn.microsoft.com/73be7109-0d3a-4ac5-adb7-e1577d8640b5">ITTAPIObjectEvent</a>
 

 

