---
UID: NF:wbemprov.IWbemHiPerfProvider.StopRefreshing
title: IWbemHiPerfProvider::StopRefreshing (wbemprov.h)
description: Stops refreshing the object or enumerator corresponding to the supplied identifier.
helpviewer_keywords: ["IWbemHiPerfProvider interface [Windows Management Instrumentation]","StopRefreshing method","IWbemHiPerfProvider.StopRefreshing","IWbemHiPerfProvider::StopRefreshing","StopRefreshing","StopRefreshing method [Windows Management Instrumentation]","StopRefreshing method [Windows Management Instrumentation]","IWbemHiPerfProvider interface","_hmm_iwbemhiperfprovider_stoprefreshing","wbemprov/IWbemHiPerfProvider::StopRefreshing","wmi.iwbemhiperfprovider_stoprefreshing"]
old-location: wmi\iwbemhiperfprovider_stoprefreshing.htm
tech.root: wmi
ms.assetid: d1de54de-b57b-4e15-84b3-96cc36bf023b
ms.date: 12/05/2018
ms.keywords: IWbemHiPerfProvider interface [Windows Management Instrumentation],StopRefreshing method, IWbemHiPerfProvider.StopRefreshing, IWbemHiPerfProvider::StopRefreshing, StopRefreshing, StopRefreshing method [Windows Management Instrumentation], StopRefreshing method [Windows Management Instrumentation],IWbemHiPerfProvider interface, _hmm_iwbemhiperfprovider_stoprefreshing, wbemprov/IWbemHiPerfProvider::StopRefreshing, wmi.iwbemhiperfprovider_stoprefreshing
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
req.dll: Wmiprvsd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemHiPerfProvider::StopRefreshing
 - wbemprov/IWbemHiPerfProvider::StopRefreshing
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiprvsd.dll
api_name:
 - IWbemHiPerfProvider.StopRefreshing
---

# IWbemHiPerfProvider::StopRefreshing


## -description

The 
<b>IWbemHiPerfProvider::StopRefreshing</b> method stops refreshing the object or enumerator corresponding to the supplied identifier. The WMI Refresher calls this method in response to a client request to <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-remove">IWbemConfiguratorRefresher::Remove</a>. The provider should check the objects and enumerators associated with the refresher for a matching identifier. When the provider finds an identifier, the provider should remove or release the enumerator.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>. A provider should implement <b>StopRefreshing</b> if it implements 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum">IWbemHiPerfProvider::CreateRefreshableEnum</a> or 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject">IWbemHiPerfProvider::CreateRefreshableObject</a>.</div><div> </div>

## -parameters

### -param pRefresher [in]

A pointer to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a> object that contains a refresher obtained by calling 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher">IWbemHiPerfProvider::CreateRefresher</a>.

### -param lId [in]

An integer containing a refresher identifier that uniquely identifies the object to stop refreshing.

### -param lFlags [in]

An integer containing the flags.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

It is not necessary to call 
<b>StopRefreshing</b> to clean up a refresher. It is sufficient simply to delete the refresher; that is, to release all references to it. Deleting the refresher causes the cleanup of all objects and enumerators within it.

## -see-also

<a href="/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Writing an Instance Provider</a>