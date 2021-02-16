---
UID: NF:wbemprov.IWbemHiPerfProvider.CreateRefresher
title: IWbemHiPerfProvider::CreateRefresher (wbemprov.h)
description: Creates a refresher.
helpviewer_keywords: ["CreateRefresher","CreateRefresher method [Windows Management Instrumentation]","CreateRefresher method [Windows Management Instrumentation]","IWbemHiPerfProvider interface","IWbemHiPerfProvider interface [Windows Management Instrumentation]","CreateRefresher method","IWbemHiPerfProvider.CreateRefresher","IWbemHiPerfProvider::CreateRefresher","_hmm_iwbemhiperfprovider_createrefresher","wbemprov/IWbemHiPerfProvider::CreateRefresher","wmi.iwbemhiperfprovider_createrefresher"]
old-location: wmi\iwbemhiperfprovider_createrefresher.htm
tech.root: wmi
ms.assetid: 5962f5f6-a121-4234-8dcd-24c0e2b53990
ms.date: 12/05/2018
ms.keywords: CreateRefresher, CreateRefresher method [Windows Management Instrumentation], CreateRefresher method [Windows Management Instrumentation],IWbemHiPerfProvider interface, IWbemHiPerfProvider interface [Windows Management Instrumentation],CreateRefresher method, IWbemHiPerfProvider.CreateRefresher, IWbemHiPerfProvider::CreateRefresher, _hmm_iwbemhiperfprovider_createrefresher, wbemprov/IWbemHiPerfProvider::CreateRefresher, wmi.iwbemhiperfprovider_createrefresher
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
 - IWbemHiPerfProvider::CreateRefresher
 - wbemprov/IWbemHiPerfProvider::CreateRefresher
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
 - IWbemHiPerfProvider.CreateRefresher
---

# IWbemHiPerfProvider::CreateRefresher


## -description

The 
<b>IWbemHiPerfProvider::CreateRefresher</b> method creates a refresher. The returned refresher will be used in subsequent calls to 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum">IWbemHiPerfProvider::CreateRefreshableEnum</a>, 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject">IWbemHiPerfProvider::CreateRefreshableObject</a>, and 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing">IWbemHiPerfProvider::StopRefreshing</a>.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>. A provider must implement this method to support refresher operations.</div><div> </div>

## -parameters

### -param pNamespace [in]

An 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. The provider should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on this pointer if it is going to call back into Windows Management during its execution.

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

### -param ppRefresher [out]

Pointer to hold the reference to the provider's implementation of the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a> interface.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

The provider must supply its own implementation of the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a> interface. It is valid for WMI to request multiple refreshers, each of which will be used for its own refresh operations.

When you release a refresher, the provider should clean up any refreshable objects or enumerators that were added to the refresher.


#### Examples

The following code example describes how to implement 
<b>CreateRefresher</b>.


```cpp
HRESULT CHiPerfProvider::CreateRefresher(
  /* [in] */IWbemServices *pNamespace,
  /* [in] */ long lFlags,
  /* [out] */ IWbemRefresher** ppRefresher
)
{
    // Allocate a new refresher
    //For Example:
    // CMyRefresher* pMyRefresher = new CMyRefresher();

    // Return the refresher to the ppRefresher
    // [out] parameter
    /*return pMyRefresher->QueryInterface(
     IID_IWbemRefresher, (void**) ppRefresher );*/
}

// Free memory resources.
// For Example:
//pNamespace->Release();
//ppRefresher->Release();
//delete[] pMyRefresher;
```

## -see-also

<a href="/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Writing an Instance Provider</a>