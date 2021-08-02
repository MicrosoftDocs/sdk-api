---
UID: NF:wbemprov.IWbemEventProviderQuerySink.CancelQuery
title: IWbemEventProviderQuerySink::CancelQuery (wbemprov.h)
description: Call the IWbemEventProviderQuerySink::CancelQuery method whenever a logical event consumer cancels a relevant event query filter with Windows Management.
helpviewer_keywords: ["CancelQuery","CancelQuery method [Windows Management Instrumentation]","CancelQuery method [Windows Management Instrumentation]","IWbemEventProviderQuerySink interface","IWbemEventProviderQuerySink interface [Windows Management Instrumentation]","CancelQuery method","IWbemEventProviderQuerySink.CancelQuery","IWbemEventProviderQuerySink::CancelQuery","_hmm_iwbemeventproviderquerysink_cancelquery","wbemprov/IWbemEventProviderQuerySink::CancelQuery","wmi.iwbemeventproviderquerysink_cancelquery"]
old-location: wmi\iwbemeventproviderquerysink_cancelquery.htm
tech.root: wmi
ms.assetid: fdb56ea9-bd1a-436e-aaa7-3ae11e10f38e
ms.date: 12/05/2018
ms.keywords: CancelQuery, CancelQuery method [Windows Management Instrumentation], CancelQuery method [Windows Management Instrumentation],IWbemEventProviderQuerySink interface, IWbemEventProviderQuerySink interface [Windows Management Instrumentation],CancelQuery method, IWbemEventProviderQuerySink.CancelQuery, IWbemEventProviderQuerySink::CancelQuery, _hmm_iwbemeventproviderquerysink_cancelquery, wbemprov/IWbemEventProviderQuerySink::CancelQuery, wmi.iwbemeventproviderquerysink_cancelquery
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
 - IWbemEventProviderQuerySink::CancelQuery
 - wbemprov/IWbemEventProviderQuerySink::CancelQuery
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
 - IWbemEventProviderQuerySink.CancelQuery
---

# IWbemEventProviderQuerySink::CancelQuery


## -description

Call the 
<b>IWbemEventProviderQuerySink::CancelQuery</b> method whenever a logical event consumer cancels a relevant event query filter with Windows Management. The 
<b>CancelQuery</b> method determines how an event provider responds to a relevant canceled event query filter. Whenever WMI retrieves a cancellation notice for an event query filter from a consumer, WMI calls 
<b>CancelQuery</b> to echo the cancellation to the responsible event provider. The event provider can examine the identifier of the query to determine which query is being canceled. The provider then modifies which events are being sent out based on the cancellation.

## -parameters

### -param dwId [in]

Identifier of the query which was canceled. This identifier was originally delivered to the provider by the 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery">NewQuery</a> method of this interface.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

Whenever a consumer registers a new event query filter, Windows Management calls the 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery">IWbemEventProviderQuerySink::NewQuery</a> method with the query identifier. Later, when that query is unregistered, this method is called indicating which query is no longer outstanding.

Providers use this method to help optimize the generation of events internally.

## -see-also

<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemeventproviderquerysink">IWbemEventProviderQuerySink</a>



<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery">IWbemEventProviderQuerySink::NewQuery</a>