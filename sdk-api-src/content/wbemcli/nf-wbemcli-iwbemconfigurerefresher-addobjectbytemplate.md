---
UID: NF:wbemcli.IWbemConfigureRefresher.AddObjectByTemplate
title: IWbemConfigureRefresher::AddObjectByTemplate (wbemcli.h)
description: With the IWbemConfigureRefresher::AddObjectByTemplate method, you can add an object you want refreshed to a refresher by specifying an IWbemClassObject instance template.
helpviewer_keywords: ["AddObjectByTemplate","AddObjectByTemplate method [Windows Management Instrumentation]","AddObjectByTemplate method [Windows Management Instrumentation]","IWbemConfigureRefresher interface","IWbemConfigureRefresher interface [Windows Management Instrumentation]","AddObjectByTemplate method","IWbemConfigureRefresher.AddObjectByTemplate","IWbemConfigureRefresher::AddObjectByTemplate","_hmm_iwbemconfigurerefresher_addobjectbytemplate","wbemcli/IWbemConfigureRefresher::AddObjectByTemplate","wmi.iwbemconfigurerefresher_addobjectbytemplate"]
old-location: wmi\iwbemconfigurerefresher_addobjectbytemplate.htm
tech.root: wmi
ms.assetid: c3f25484-7c6c-4625-9d26-1c01d15b10c4
ms.date: 12/05/2018
ms.keywords: AddObjectByTemplate, AddObjectByTemplate method [Windows Management Instrumentation], AddObjectByTemplate method [Windows Management Instrumentation],IWbemConfigureRefresher interface, IWbemConfigureRefresher interface [Windows Management Instrumentation],AddObjectByTemplate method, IWbemConfigureRefresher.AddObjectByTemplate, IWbemConfigureRefresher::AddObjectByTemplate, _hmm_iwbemconfigurerefresher_addobjectbytemplate, wbemcli/IWbemConfigureRefresher::AddObjectByTemplate, wmi.iwbemconfigurerefresher_addobjectbytemplate
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
 - IWbemConfigureRefresher::AddObjectByTemplate
 - wbemcli/IWbemConfigureRefresher::AddObjectByTemplate
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
 - IWbemConfigureRefresher.AddObjectByTemplate
---

# IWbemConfigureRefresher::AddObjectByTemplate


## -description

With the 
<b>IWbemConfigureRefresher::AddObjectByTemplate</b> method, you can add an object you want refreshed to a refresher by specifying an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> instance template. Use this method when it is difficult to construct an object path for an object to add to a refresher.
<div class="alert"><b>Note</b>  The key properties of the instance object must be filled out before you can call the 
<b>AddObjectByTemplate</b> method.</div><div> </div>

## -parameters

### -param pNamespace

An 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. The provider should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on this pointer if it is going to call back into Windows Management during its execution.

### -param pTemplate [in]

Pointer to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object that contains the instance template.

### -param lFlags [in]

Bitmask of flags that modify the behavior of this method. If this parameter is set to <b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b>, the returned instance will contain localized qualifiers if available.

### -param pContext [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the specific provider documentation. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppRefreshable [out]

Pointer to hold the reference to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object, which will contain the refreshable instance object. The client must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned object when it is no longer required.

### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies this refreshable object.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

The supplied instance must specify a valid object, which is provided by the High-Performance Provider. The returned object must not be modified by the client while a refresh operation is in process. The returned identifier can be used by the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-remove">Remove</a> function to remove the object.

It is not necessary for the user to explicitly remove added objects. The client must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned object when it is no longer required.

## -see-also

<a href="/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemconfigurerefresher">IWbemConfigureRefresher</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Making an Instance Provider into a High-Performance Provider</a>



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>