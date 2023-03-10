---
UID: NF:wbemprov.IWbemProviderInitSink.SetStatus
title: IWbemProviderInitSink::SetStatus (wbemprov.h)
description: The IWbemProviderInitSink::SetStatus method indicates to Windows Management whether a provider is fully or partially initialized.
helpviewer_keywords: ["IWbemProviderInitSink interface [Windows Management Instrumentation]","SetStatus method","IWbemProviderInitSink.SetStatus","IWbemProviderInitSink::SetStatus","SetStatus","SetStatus method [Windows Management Instrumentation]","SetStatus method [Windows Management Instrumentation]","IWbemProviderInitSink interface","WBEM_E_FAILED","WBEM_S_INITIALIZED","_hmm_iwbemproviderinitsink_setstatus","wbemprov/IWbemProviderInitSink::SetStatus","wmi.iwbemproviderinitsink_setstatus"]
old-location: wmi\iwbemproviderinitsink_setstatus.htm
tech.root: wmi
ms.assetid: 909935ba-ae3a-477d-a466-1f2679764b10
ms.date: 12/05/2018
ms.keywords: IWbemProviderInitSink interface [Windows Management Instrumentation],SetStatus method, IWbemProviderInitSink.SetStatus, IWbemProviderInitSink::SetStatus, SetStatus, SetStatus method [Windows Management Instrumentation], SetStatus method [Windows Management Instrumentation],IWbemProviderInitSink interface, WBEM_E_FAILED, WBEM_S_INITIALIZED, _hmm_iwbemproviderinitsink_setstatus, wbemprov/IWbemProviderInitSink::SetStatus, wmi.iwbemproviderinitsink_setstatus
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
 - IWbemProviderInitSink::SetStatus
 - wbemprov/IWbemProviderInitSink::SetStatus
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
 - IWbemProviderInitSink.SetStatus
---

# IWbemProviderInitSink::SetStatus


## -description

The 
<b>IWbemProviderInitSink::SetStatus</b> method indicates to Windows Management whether a provider is fully or partially initialized.

## -parameters

### -param lStatus [in]

Indicates to Windows Management a provider's initialization status. One of the following values can be set.



#### WBEM_S_INITIALIZED

Indicates that the provider is fully initialized and ready to accept requests.



#### WBEM_E_FAILED

Indicates that the provider has failed to initialize and is not functional.

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

## -returns

This method always returns <b>WBEM_S_NO_ERROR</b>.

## -remarks

All types of providers call 
<b>IWbemProviderInitSink::SetStatus</b> to indicate initialization status to Windows Management.

If <i>lStatus</i> is set to <b>WBEM_S_INITIALIZED</b>, Windows Management expects the provider to be fully capable of immediately servicing requests.

## -see-also

<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinitsink">IWbemProviderInitSink</a>



<a href="/windows/desktop/WmiSdk/initializing-a-provider">Initializing a Provider</a>