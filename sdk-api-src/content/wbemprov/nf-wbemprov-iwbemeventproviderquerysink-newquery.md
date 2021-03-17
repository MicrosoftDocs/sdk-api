---
UID: NF:wbemprov.IWbemEventProviderQuerySink.NewQuery
title: IWbemEventProviderQuerySink::NewQuery (wbemprov.h)
description: Call the IWbemEventProviderQuerySink::NewQuery method when a logical event consumer registers a relevant event query filter with Windows Management.
helpviewer_keywords: ["IWbemEventProviderQuerySink interface [Windows Management Instrumentation]","NewQuery method","IWbemEventProviderQuerySink.NewQuery","IWbemEventProviderQuerySink::NewQuery","NewQuery","NewQuery method [Windows Management Instrumentation]","NewQuery method [Windows Management Instrumentation]","IWbemEventProviderQuerySink interface","_hmm_iwbemeventproviderquerysink_newquery","wbemprov/IWbemEventProviderQuerySink::NewQuery","wmi.iwbemeventproviderquerysink_newquery"]
old-location: wmi\iwbemeventproviderquerysink_newquery.htm
tech.root: wmi
ms.assetid: 82f76b19-2035-4567-b619-31ce8a35e422
ms.date: 12/05/2018
ms.keywords: IWbemEventProviderQuerySink interface [Windows Management Instrumentation],NewQuery method, IWbemEventProviderQuerySink.NewQuery, IWbemEventProviderQuerySink::NewQuery, NewQuery, NewQuery method [Windows Management Instrumentation], NewQuery method [Windows Management Instrumentation],IWbemEventProviderQuerySink interface, _hmm_iwbemeventproviderquerysink_newquery, wbemprov/IWbemEventProviderQuerySink::NewQuery, wmi.iwbemeventproviderquerysink_newquery
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
 - IWbemEventProviderQuerySink::NewQuery
 - wbemprov/IWbemEventProviderQuerySink::NewQuery
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
 - IWbemEventProviderQuerySink.NewQuery
---

# IWbemEventProviderQuerySink::NewQuery


## -description

Call the 
<b>IWbemEventProviderQuerySink::NewQuery</b> method when a logical event consumer registers a relevant event query filter with Windows Management. The 
<b>NewQuery</b> method determines how a provider responds to a new query registered by a client application. When WMI receives a new or modified event query from a consumer, WMI calls 
<b>NewQuery</b> to echo the query to the event provider. The provider then generates the requested notification.

## -parameters

### -param dwId [in]

Windows Management-generated identifier for the query. The provider can track this so that during a later call to 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery">CancelQuery</a> so that the provider will know which query was canceled.

### -param wszQueryLanguage [in]

Language of the following query filter. For this version of WMI, it will always be "WQL".

### -param wszQuery [in]

Text of the event query filter, which was registered by a logical consumer. The event provider can examine the text of the query filter through the <i>wszQuery</i> parameter and the language of the query filter in the <i>wszQueryLanguage</i> parameter to discover which event notifications the consumer is requesting.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists return codes returned by 
<b>NewQuery</b>. Additionally, a third-party event provider could return any valid WMI or COM return code which could be passed through 
<b>NewQuery</b> as a return value.

## -remarks

If a consumer registers an event filter query with Windows Management and the query contains references to events provided by the current event provider, Windows Management can notify the event provider of the query.

If the provider implements the 
<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemeventproviderquerysink">IWbemEventProviderQuerySink</a> interface, Windows Management will provide a copy of the query text to the provider. The provider should parse the query, and determine if it can perform any internal optimization.

Windows Management does not expect a provider to alter its behavior in any way. Rather, this is an advisory call to assist the provider with internal optimization.

For example, if the provider is capable of providing many hundreds of events, but the required overhead for providing all of them is great, the provider can achieve substantial savings if it knows that most of these events are not required by the current set of event consumers. If the provider implements 
<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemeventproviderquerysink">IWbemEventProviderQuerySink</a>, it will know about the current set of events requested by all consumers. It may be able to avoid setting up the mechanisms for delivering most of the event types that it supports until consumers actually begin requesting such events.

For each new consumer query filter, a separate call to this method with a unique dwId will be made. Be aware that Windows Management reserves the right to call 
<b>NewQuery</b> more than one time for the same dwId value; for example, if there is a schema change elsewhere in the system. For this version of WMI, the query language is always "WQL".

The 
<b>IWbemEventProviderQuerySink::NewQuery</b> method can be called before the 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventprovider-provideevents">IWbemEventProvider::ProvideEvents</a> method.

## -see-also

<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemeventproviderquerysink">IWbemEventProviderQuerySink</a>



<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery">IWbemEventProviderQuerySink::CancelQuery</a>