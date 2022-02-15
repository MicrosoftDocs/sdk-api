---
UID: NF:wbemprov.IWbemEventProvider.ProvideEvents
title: IWbemEventProvider::ProvideEvents (wbemprov.h)
description: Windows Management calls the IWbemEventProvider::ProvideEvents method to signal an event provider to begin delivery of its events.
helpviewer_keywords: ["IWbemEventProvider interface [Windows Management Instrumentation]","ProvideEvents method","IWbemEventProvider.ProvideEvents","IWbemEventProvider::ProvideEvents","ProvideEvents","ProvideEvents method [Windows Management Instrumentation]","ProvideEvents method [Windows Management Instrumentation]","IWbemEventProvider interface","_hmm_iwbemeventprovider_provideevents","wbemprov/IWbemEventProvider::ProvideEvents","wmi.iwbemeventprovider_provideevents"]
old-location: wmi\iwbemeventprovider_provideevents.htm
tech.root: wmi
ms.assetid: 0ebabdaf-fd91-49f8-8454-38ff77952662
ms.date: 12/05/2018
ms.keywords: IWbemEventProvider interface [Windows Management Instrumentation],ProvideEvents method, IWbemEventProvider.ProvideEvents, IWbemEventProvider::ProvideEvents, ProvideEvents, ProvideEvents method [Windows Management Instrumentation], ProvideEvents method [Windows Management Instrumentation],IWbemEventProvider interface, _hmm_iwbemeventprovider_provideevents, wbemprov/IWbemEventProvider::ProvideEvents, wmi.iwbemeventprovider_provideevents
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
 - IWbemEventProvider::ProvideEvents
 - wbemprov/IWbemEventProvider::ProvideEvents
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
 - IWbemEventProvider.ProvideEvents
---

# IWbemEventProvider::ProvideEvents


## -description

Windows Management calls the 
<b>IWbemEventProvider::ProvideEvents</b> method to signal an event provider to begin delivery of its events.

## -parameters

### -param pSink [in]

Pointer to the object sink to which the provider will deliver its events. In an event provider implementation, you should use the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> method to send events through <i>pSink</i>. This is in contrast to other providers that may use the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> method: The 
<b>ProvideEvents</b> method should use only 
<b>Indicate</b> to update a sink.

### -param lFlags [in]

Reserved. This parameter must be 0.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

Windows Management calls this method to activate the provider. Windows Management gives an 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> pointer to the event provider. The provider must call the <b>AddRef</b> method using this pointer to increment the reference count, and then return from the call.

Typically, the provider will create an independent thread, and deliver the events as they occur to the provided sink interface.

The provider is not permitted to block this call for more than a few seconds, but it must return as quickly as possible to Windows Management.