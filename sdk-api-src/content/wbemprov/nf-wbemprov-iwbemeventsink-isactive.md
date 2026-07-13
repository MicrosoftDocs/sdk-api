---
UID: NF:wbemprov.IWbemEventSink.IsActive
title: IWbemEventSink::IsActive (wbemprov.h)
description: The IWbemEventSink::IsActive method is used by the provider to determine if there is interest in the events that the sink is filtering.
helpviewer_keywords: ["IWbemEventSink interface [Windows Management Instrumentation]","IsActive method","IWbemEventSink.IsActive","IWbemEventSink::IsActive","IsActive","IsActive method [Windows Management Instrumentation]","IsActive method [Windows Management Instrumentation]","IWbemEventSink interface","_hmm_iwbemeventsink_isactive","wbemprov/IWbemEventSink::IsActive","wmi.iwbemeventsink_isactive"]
old-location: wmi\iwbemeventsink_isactive.htm
tech.root: wmi
ms.assetid: dc5afbc1-60da-42ec-9dc3-79b66243690c
ms.date: 12/05/2018
ms.keywords: IWbemEventSink interface [Windows Management Instrumentation],IsActive method, IWbemEventSink.IsActive, IWbemEventSink::IsActive, IsActive, IsActive method [Windows Management Instrumentation], IsActive method [Windows Management Instrumentation],IWbemEventSink interface, _hmm_iwbemeventsink_isactive, wbemprov/IWbemEventSink::IsActive, wmi.iwbemeventsink_isactive
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
 - IWbemEventSink::IsActive
 - wbemprov/IWbemEventSink::IsActive
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
 - IWbemEventSink.IsActive
---

# IWbemEventSink::IsActive


## -description

The 
<b>IWbemEventSink::IsActive</b> method is used by the provider to determine if there is interest in the events that the sink is filtering. In the case of a restricted sink, these events are defined by the queries passed to 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink">GetRestrictedSink</a>. In the case where it is not a restricted sink, these events are defined by the queries in the event provider's registration. In the latter, the sink is always active.



## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.
