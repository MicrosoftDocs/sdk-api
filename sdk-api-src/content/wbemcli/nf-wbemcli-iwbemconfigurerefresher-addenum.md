---
UID: NF:wbemcli.IWbemConfigureRefresher.AddEnum
title: IWbemConfigureRefresher::AddEnum (wbemcli.h)
description: The IWbemConfigureRefresher::AddEnum method adds an enumerator to the requested refresher.
helpviewer_keywords: ["AddEnum","AddEnum method [Windows Management Instrumentation]","AddEnum method [Windows Management Instrumentation]","IWbemConfigureRefresher interface","IWbemConfigureRefresher interface [Windows Management Instrumentation]","AddEnum method","IWbemConfigureRefresher.AddEnum","IWbemConfigureRefresher::AddEnum","_hmm_iwbemconfigurerefresher_addenum","wbemcli/IWbemConfigureRefresher::AddEnum","wmi.iwbemconfigurerefresher_addenum"]
old-location: wmi\iwbemconfigurerefresher_addenum.htm
tech.root: wmi
ms.assetid: 5b013267-78bc-4372-b55a-58e330acf927
ms.date: 12/05/2018
ms.keywords: AddEnum, AddEnum method [Windows Management Instrumentation], AddEnum method [Windows Management Instrumentation],IWbemConfigureRefresher interface, IWbemConfigureRefresher interface [Windows Management Instrumentation],AddEnum method, IWbemConfigureRefresher.AddEnum, IWbemConfigureRefresher::AddEnum, _hmm_iwbemconfigurerefresher_addenum, wbemcli/IWbemConfigureRefresher::AddEnum, wmi.iwbemconfigurerefresher_addenum
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
 - IWbemConfigureRefresher::AddEnum
 - wbemcli/IWbemConfigureRefresher::AddEnum
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
 - IWbemConfigureRefresher.AddEnum
---

# IWbemConfigureRefresher::AddEnum


## -description

The 
<b>IWbemConfigureRefresher::AddEnum</b> method adds an enumerator to the requested refresher.

## -parameters

### -param pNamespace [in]

An 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. If the method must call back into Windows Management during its execution, the provider should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> with the <i>pNamespace</i> pointer.

### -param wszClassName [in]

Constant, null-terminated string of 16-bit Unicode characters containing the name of the class that is enumerated.

### -param lFlags [in]

Bitmask of flags that modify the behavior of this method. If this parameter is set to WBEM_FLAG_USE_AMENDED_QUALIFIERS, the returned instances contain localized qualifiers if they are available.

### -param pContext [in]

Typically <b>NULL</b>; otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the specific provider documentation. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppEnum [out]

Pointer that holds the reference to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemhiperfenum">IWbemHiPerfEnum</a> object, which will contain the enumeration. The client must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on this pointer when it is no longer required.

### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies the refreshable enumeration.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <div class="alert"><b>Note</b>  <b>HRESULT</b></div>
<div> </div>.

## -remarks

The supplied class must specify a valid class, which is provided by the High-Performance Provider. All instances of the returned enumerator can be queried after calls. On each call to refresh, the number of instances in the enumerator can vary. Only instances of the specified class name are returned; subclasses of the specified class will not be enumerated because detailed enumeration is not supported. The returned enumerator must not be touched by the client while a 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">Refresh</a> operation is in process. The returned identifier can be used by the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-remove">Remove</a> function to remove the object. Note that it is not necessary for the user to explicitly remove added enumerators. However, the client must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned enumerator when it is no longer required.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemconfigurerefresher">IWbemConfigureRefresher</a>