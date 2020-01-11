---
UID: NF:evntprov.EventEnabled
title: EventEnabled function (evntprov.h)
description: Determines if the event is enabled for any session.
old-location: etw\eventenabled_func.htm
tech.root: ETW
ms.assetid: b332b6d4-6921-40bd-bebc-6646b5b9bcde
ms.date: 12/05/2018
ms.keywords: EventEnabled, EventEnabled function [ETW], base.eventenabled_func, etw.eventenabled_func, evntprov/EventEnabled
f1_keywords:
- evntprov/EventEnabled
dev_langs:
- c++
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
- API-MS-Win-eventing-provider-l1-1-0.dll
- API-MS-Win-Eventing-Provider-L1-1-1.dll
- bcrypt.dll
api_name:
- EventEnabled
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventEnabled function


## -description


Determines if the event is enabled for any session.


## -parameters




### -param RegHandle [in]

Registration handle of the provider. The handle comes from 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>.

<div class="alert"><b>Note</b>  A valid registration handle 
      must be used.</div>
<div> </div>

### -param EventDescriptor [in]

Describes the event. For details, see <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>. 


## -returns



Returns <b>TRUE</b> if the event is enabled for a session; otherwise, <b>FALSE</b>.




## -remarks



Typically, providers do not call this function to determine if a session is expecting this event, they simply 
    write the event and ETW determines if the event is logged to the session. 

Providers may want to call this function if they need to perform extra work to generate the event. Calling 
    this function first to determine if a session is expecting this event or not, may save resources and time.

The provider would call this function if the provider generated an 
    <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a> structure for the event from the 
    manifest. If the event descriptor is not available, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventproviderenabled">EventProviderEnabled</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventproviderenabled">EventProviderEnabled</a>
 

 

