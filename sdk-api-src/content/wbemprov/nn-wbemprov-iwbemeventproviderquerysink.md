---
UID: NN:wbemprov.IWbemEventProviderQuerySink
title: IWbemEventProviderQuerySink (wbemprov.h)
description: The IWbemEventProviderQuerySink interface is optionally implemented by event providers who want to know what kinds of event query filters are currently active to optimize performance.
helpviewer_keywords: ["IWbemEventProviderQuerySink","IWbemEventProviderQuerySink interface [Windows Management Instrumentation]","IWbemEventProviderQuerySink interface [Windows Management Instrumentation]","described","_hmm_iwbemeventproviderquerysink","wbemprov/IWbemEventProviderQuerySink","wmi.iwbemeventproviderquerysink"]
old-location: wmi\iwbemeventproviderquerysink.htm
tech.root: wmi
ms.assetid: 76a29d81-33c2-489f-a71d-2e85ba2617bf
ms.date: 12/05/2018
ms.keywords: IWbemEventProviderQuerySink, IWbemEventProviderQuerySink interface [Windows Management Instrumentation], IWbemEventProviderQuerySink interface [Windows Management Instrumentation],described, _hmm_iwbemeventproviderquerysink, wbemprov/IWbemEventProviderQuerySink, wmi.iwbemeventproviderquerysink
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
 - IWbemEventProviderQuerySink
 - wbemprov/IWbemEventProviderQuerySink
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
 - IWbemEventProviderQuerySink
---

# IWbemEventProviderQuerySink interface


## -description

The 
<b>IWbemEventProviderQuerySink</b> interface is optionally implemented by event providers who want to know what kinds of event query filters are currently active to optimize performance.

## -inheritance

The <b>IWbemEventProviderQuerySink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemEventProviderQuerySink</b> also has these types of members:

## -remarks

Although WMI calls the methods of 
<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemeventprovider">IWbemEventProvider</a> only one time after an event provider becomes active, WMI calls the methods of 
<b>IWbemEventProviderQuerySink</b> continuously, as appropriate. The provider can ignore all calls to 
<b>IWbemEventProviderQuerySink</b> methods as needed. This point is very important; supporting 
<b>IWbemEventProviderQuerySink</b> indicates that a provider will supply at least the events requested by queries.

A provider can also generate more events than requested, which WMI filters as appropriate. This functionality means you can implement 
<b>IWbemEventProviderQuerySink</b> and optimize processing without addressing all parts of the WMI Query Language (WQL). For instance, if a provider does not specifically handle a particular query, the provider can generate all possible events for the query.
