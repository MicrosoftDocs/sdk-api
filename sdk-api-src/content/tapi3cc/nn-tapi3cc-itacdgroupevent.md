---
UID: NN:tapi3cc.ITACDGroupEvent
title: ITACDGroupEvent
author: windows-sdk-content
description: The ITACDGroupEvent interface contains methods that retrieve the description of Automatic Call Distribution (ACD) group events.
old-location: tapi3\itacdgroupevent.htm
old-project: Tapi
ms.assetid: 5770dca5-cf71-4211-ba9f-0fe7a3bbb614
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITACDGroupEvent, ITACDGroupEvent interface [TAPI 2.2], ITACDGroupEvent interface [TAPI 2.2],described, _tapi3_itacdgroupevent, tapi3.itacdgroupevent, tapi3cc/ITACDGroupEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3cc.h
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
req.typenames: AGENT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITACDGroupEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITACDGroupEvent interface


## -description


The 
<b>ITACDGroupEvent</b> interface contains methods that retrieve the description of Automatic Call Distribution (ACD) group events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_ACDGROUP</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITACDGroupEvent</b> interface. The methods of this interface can be used to retrieve information concerning the ACD group change that has occurred.

See 
<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a> for additional information concerning ACD groups.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_ACDGROUP</b> event to enable reception of ACD group events. If you do not call ITTAPI::put_EventFilter, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITACDGroupEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch.md">IDispatch</a> interface. <b>ITACDGroupEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITACDGroupEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bc67911-cfb6-450c-bdc6-ade8d4617271">get_Event</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/fb3de7e5-5a29-4f7b-8b2a-252536dedae6">ACDGROUP_EVENT</a> descriptor of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbdc94b0-fa46-422a-bffc-32bbd1d49e5a">get_Group</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fb3de7e5-5a29-4f7b-8b2a-252536dedae6">ACDGROUP_EVENT</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch.md">IDispatch</a>



<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

