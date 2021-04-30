---
UID: NF:evntprov.EventUnregister
title: EventUnregister function (evntprov.h)
description: Removes the provider's registration. You must call this function before your process exits.
helpviewer_keywords: ["EventUnregister","EventUnregister function [ETW]","base.eventunregister_func","etw.eventunregister_func","evntprov/EventUnregister"]
old-location: etw\eventunregister_func.htm
tech.root: ETW
ms.assetid: fdcccf6f-2f31-4356-a4ee-3b6229c01b75
ms.date: 12/05/2018
ms.keywords: EventUnregister, EventUnregister function [ETW], base.eventunregister_func, etw.eventunregister_func, evntprov/EventUnregister
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EventUnregister
 - evntprov/EventUnregister
dev_langs:
 - c++
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
 - rtmpal.dll
api_name:
 - EventUnregister
---

# EventUnregister function


## -description

Removes the provider's registration. You must call this function before your process exits.

## -parameters

### -param RegHandle [in]

Registration handle returned by 
      <a href="/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>.

## -returns

Returns ERROR_SUCCESS if successful.

## -remarks

For private sessions, you must stop the trace (call the 
    <a href="/windows/desktop/ETW/controltrace">ControlTrace</a> function with the 
    <i>ControlCode</i> parameter set to EVENT_TRACE_CONTROL_STOP) before calling this 
    function.

## -see-also

<a href="/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>