---
UID: NF:evntprov.EventRegister
title: EventRegister function (evntprov.h)
description: Registers the provider.
helpviewer_keywords: ["EventRegister","EventRegister function [ETW]","base.eventregister_func","etw.eventregister_func","evntprov/EventRegister"]
old-location: etw\eventregister_func.htm
tech.root: ETW
ms.assetid: 6025c3a6-7d88-49dc-bbc3-655c172dde3c
ms.date: 12/05/2018
ms.keywords: EventRegister, EventRegister function [ETW], base.eventregister_func, etw.eventregister_func, evntprov/EventRegister
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
 - EventRegister
 - evntprov/EventRegister
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
 - EventRegister
---

# EventRegister function


## -description

Registers the provider.

## -parameters

### -param ProviderId [in]

GUID that uniquely identifies the provider.

### -param EnableCallback [in, optional]

Callback that ETW  calls to notify you when a session enables or disables your provider. Can be 
      <b>NULL</b>.

### -param CallbackContext [in, optional]

Provider-defined context data to pass to the callback when the provider is enabled or disabled. Can be 
      <b>NULL</b>.

### -param RegHandle [out]

Registration handle. The handle is used by most provider function calls. Before your provider exits, you 
      must pass this handle to <a href="/windows/desktop/api/evntprov/nf-evntprov-eventunregister">EventUnregister</a> to 
      free the handle.

## -returns

Returns ERROR_SUCCESS if successful.

## -remarks

Use this function to register your provider if you call 
    <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a> to write your events.

A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that 
     your process registers to one or two. This limit includes those registered using this function and the 
     <a href="/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> function.

<b>Prior to Windows Vista:  </b>There is no limit to the number of providers that a process can register.

## -see-also

<a href="/windows/desktop/api/evntprov/nc-evntprov-penablecallback">EnableCallback</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventunregister">EventUnregister</a>