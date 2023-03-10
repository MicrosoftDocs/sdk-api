---
UID: NN:wbemprov.IWbemEventSink
title: IWbemEventSink (wbemprov.h)
description: Initiates communication with an event provider using a restricted set of queries.
helpviewer_keywords: ["IWbemEventSink","IWbemEventSink interface [Windows Management Instrumentation]","IWbemEventSink interface [Windows Management Instrumentation]","described","_hmm_iwbemeventsink","wbemprov/IWbemEventSink","wmi.iwbemeventsink"]
old-location: wmi\iwbemeventsink.htm
tech.root: wmi
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.date: 12/05/2018
ms.keywords: IWbemEventSink, IWbemEventSink interface [Windows Management Instrumentation], IWbemEventSink interface [Windows Management Instrumentation],described, _hmm_iwbemeventsink, wbemprov/IWbemEventSink, wmi.iwbemeventsink
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemEventSink
 - wbemprov/IWbemEventSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventSink
---

# IWbemEventSink interface


## -description

The 
<b>IWbemEventSink</b> interface initiates communication with an event provider using a restricted set of queries. This interface extends 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>, providing new methods dealing with security and performance. For more information about using this interface, see <a href="/windows/desktop/WmiSdk/writing-an-event-provider">Writing an Event Provider</a> and <a href="/windows/desktop/WmiSdk/securing-wmi-events">Securing WMI Events</a>.

## -inheritance

The <b>IWbemEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemEventSink</b> also has these types of members:

## -remarks

When implementing an event subscription sink (<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> or <b>IWbemEventSink</b>), do  not call into WMI from within the  methods on the sink object.  For example, calling <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-cancelasynccall">IWbemServices::CancelAsyncCall</a> to cancel the sink  from within an implementation of <a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity">IWbemEventSink::SetSinkSecurity</a> can interfere with the WMI state. To cancel an event subscription, set a flag and call <b>IWbemServices::CancelAsyncCall</b> from another thread or object. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing. If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>
