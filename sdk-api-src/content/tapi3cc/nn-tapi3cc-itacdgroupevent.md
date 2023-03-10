---
UID: NN:tapi3cc.ITACDGroupEvent
title: ITACDGroupEvent (tapi3cc.h)
description: The ITACDGroupEvent interface (tapi3cc.h) contains methods that retrieve the description of Automatic Call Distribution (ACD) group events.
helpviewer_keywords: ["ITACDGroupEvent","ITACDGroupEvent interface [TAPI 2.2]","ITACDGroupEvent interface [TAPI 2.2]","described","_tapi3_itacdgroupevent","tapi3.itacdgroupevent","tapi3cc/ITACDGroupEvent"]
old-location: tapi3\itacdgroupevent.htm
tech.root: tapi3
ms.assetid: 5770dca5-cf71-4211-ba9f-0fe7a3bbb614
ms.date: 08/10/2022
ms.keywords: ITACDGroupEvent, ITACDGroupEvent interface [TAPI 2.2], ITACDGroupEvent interface [TAPI 2.2],described, _tapi3_itacdgroupevent, tapi3.itacdgroupevent, tapi3cc/ITACDGroupEvent
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITACDGroupEvent
 - tapi3cc/ITACDGroupEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITACDGroupEvent
---

# ITACDGroupEvent interface


## -description

The 
<b>ITACDGroupEvent</b> interface contains methods that retrieve the description of Automatic Call Distribution (ACD) group events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_ACDGROUP</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITACDGroupEvent</b> interface. The methods of this interface can be used to retrieve information concerning the ACD group change that has occurred.

See 
<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information concerning ACD groups.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_ACDGROUP</b> event to enable reception of ACD group events. If you do not call ITTAPI::put_EventFilter, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITACDGroupEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITACDGroupEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-acdgroup_event">ACDGROUP_EVENT</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
