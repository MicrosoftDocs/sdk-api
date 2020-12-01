---
UID: NF:wbemcli.IWbemConfigureRefresher.Remove
title: IWbemConfigureRefresher::Remove (wbemcli.h)
description: The IWbemConfigureRefresher::Remove method is used to remove an object, enumerator, or nested refresher from a refresher.
helpviewer_keywords: ["IWbemConfigureRefresher interface [Windows Management Instrumentation]","Remove method","IWbemConfigureRefresher.Remove","IWbemConfigureRefresher::Remove","Remove","Remove method [Windows Management Instrumentation]","Remove method [Windows Management Instrumentation]","IWbemConfigureRefresher interface","_hmm_iwbemconfigurerefresher_remove","wbemcli/IWbemConfigureRefresher::Remove","wmi.iwbemconfigurerefresher_remove"]
old-location: wmi\iwbemconfigurerefresher_remove.htm
tech.root: wmi
ms.assetid: f6e68b95-e9d1-473e-add4-823b6db51709
ms.date: 12/05/2018
ms.keywords: IWbemConfigureRefresher interface [Windows Management Instrumentation],Remove method, IWbemConfigureRefresher.Remove, IWbemConfigureRefresher::Remove, Remove, Remove method [Windows Management Instrumentation], Remove method [Windows Management Instrumentation],IWbemConfigureRefresher interface, _hmm_iwbemconfigurerefresher_remove, wbemcli/IWbemConfigureRefresher::Remove, wmi.iwbemconfigurerefresher_remove
req.header: wbemcli.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemConfigureRefresher::Remove
 - wbemcli/IWbemConfigureRefresher::Remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemConfigureRefresher.Remove
---

# IWbemConfigureRefresher::Remove


## -description

The 
<b>IWbemConfigureRefresher::Remove</b> method is used to remove an object, enumerator, or nested refresher from a refresher.

## -parameters

### -param lId [in]

Integer that uniquely identifies the object to remove. You obtain this identifier when you first add an object to the refresher by calling 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath">IWbemConfigureRefresher::AddObjectByPath</a>, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbytemplate">IWbemConfigureRefresher::AddObjectByTemplate</a>, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum">IWbemConfigureRefresher::AddEnum</a>, or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addrefresher">IWbemConfigureRefresher::AddRefresher</a>.

### -param lFlags [in]

Bitmask of flags that modify the behavior of the 
<b>Remove</b> method. If this parameter is set to. <b>WBEM_FLAG_REFRESH_AUTO_RECONNECT</b>, the refresher attempts to automatically reconnect to a remote provider if the connection is broken. This is default behavior for this method. Specify <b>WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT</b> if you do not want the refresher to attempt to reconnect to a remote provider.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemconfigurerefresher">IWbemConfigureRefresher</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Making an Instance Provider into a High-Performance Provider</a>



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>