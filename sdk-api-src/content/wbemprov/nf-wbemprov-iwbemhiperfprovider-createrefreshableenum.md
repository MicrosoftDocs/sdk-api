---
UID: NF:wbemprov.IWbemHiPerfProvider.CreateRefreshableEnum
title: IWbemHiPerfProvider::CreateRefreshableEnum (wbemprov.h)
description: Creates a new refreshable enumeration.
helpviewer_keywords: ["CreateRefreshableEnum","CreateRefreshableEnum method [Windows Management Instrumentation]","CreateRefreshableEnum method [Windows Management Instrumentation]","IWbemHiPerfProvider interface","IWbemHiPerfProvider interface [Windows Management Instrumentation]","CreateRefreshableEnum method","IWbemHiPerfProvider.CreateRefreshableEnum","IWbemHiPerfProvider::CreateRefreshableEnum","_hmm_iwbemhiperfprovider_createrefreshableenum","wbemprov/IWbemHiPerfProvider::CreateRefreshableEnum","wmi.iwbemhiperfprovider_createrefreshableenum"]
old-location: wmi\iwbemhiperfprovider_createrefreshableenum.htm
tech.root: wmi
ms.assetid: 086a1717-b6e8-45c1-9397-ec894ee900a0
ms.date: 12/05/2018
ms.keywords: CreateRefreshableEnum, CreateRefreshableEnum method [Windows Management Instrumentation], CreateRefreshableEnum method [Windows Management Instrumentation],IWbemHiPerfProvider interface, IWbemHiPerfProvider interface [Windows Management Instrumentation],CreateRefreshableEnum method, IWbemHiPerfProvider.CreateRefreshableEnum, IWbemHiPerfProvider::CreateRefreshableEnum, _hmm_iwbemhiperfprovider_createrefreshableenum, wbemprov/IWbemHiPerfProvider::CreateRefreshableEnum, wmi.iwbemhiperfprovider_createrefreshableenum
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
 - IWbemHiPerfProvider::CreateRefreshableEnum
 - wbemprov/IWbemHiPerfProvider::CreateRefreshableEnum
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
 - IWbemHiPerfProvider.CreateRefreshableEnum
---

# IWbemHiPerfProvider::CreateRefreshableEnum


## -description

The 
<b>IWbemHiPerfProvider::CreateRefreshableEnum</b> method creates a new refreshable enumeration. The WMI Refresher calls this method in response to a client request to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum">IWbemConfigureRefresher::AddEnum</a>. The provider associates the supplied 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemhiperfenum">IWbemHiPerfEnum</a> object with the supplied refresher. On each call to the supplied refresher's 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">Refresh</a> method, the provider ensures that the enumerator contains a set of all the instances of the class listed in the <i>wszClass</i> parameter and that these instances contain updated information. One possible way to do this would be to keep an array of refreshable enumerators in the refresher.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.</div><div> </div>

## -parameters

### -param pNamespace [in]

An 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer back into Windows Management, which can service any requests made by the provider. If <i>pNamespace</i> must call back into Windows Management during its execution, the provider calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on this pointer.

### -param wszClass [in]

Constant, <b>null</b>-terminated string of 16-bit, Unicode characters that contains the name of the class, whose instances are refreshed in the <i>pHiPerfEnum </i> parameter.

### -param pRefresher [in]

Pointer to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a> object that contains a refresher obtained by calling 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher">IWbemHiPerfProvider::CreateRefresher</a>.

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

### -param pContext [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object required by one or more dynamic class providers. The values in the context object must be specified in the specific provider's documentation. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pHiPerfEnum [in]

Pointer to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemhiperfenum">IWbemHiPerfEnum</a> object that contains the high-performance enumeration.

### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies the refreshable enumeration.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

The provider must not modify the refreshable enumerator except during a refresh operation. The enumeration is shallow, so all instances placed in the enumerator should be of the class specified by <i>wszClass</i>.

The provider must not access the enumerator unless WMI calls the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">IWbemRefresher::Refresh</a> method of the owner. As with refreshable objects, the provider must not update the enumerator unless the object owning the enumerator refreshes the enumerator.


#### Examples

The following code example describes how to implement 
<b>CreateRefreshableEnum</b>.


```cpp
HRESULT CHiPerfProvider::CreateRefreshableEnum(
  /* [in] */IWbemServices *pNamespace,
  /* [in] */LPCWSTR wszClass,
  /* [in] */IWbemRefresher *pRefresher,
  /* [in] */long lFlags,
  /* [in] */IWbemContext *pCtx,
  /* [in] */IWbemHiPerfEnum *pEnum,
  /* [out] */ long *plId
)
{
  // Use a private interface defined
  // to talk with the refresher.
  IMyRefresher* pMyRefr = NULL;

  HRESULT hres = pRefresher->QueryInterface(
    IID_IMyRefresher,
    (void**) &pMyRefr );

  if ( SUCCEEDED( hres ) )
  {
  LPLONG plLastId;
    // Generates a unique identifier
    *plId = InterlockedIncrement( &plLastId );

    // Use an internal method to add the
    // enumerator to an array.
    pMyRefr->AddEnum( wszClass, *plId, pEnum );

    pMyRefr->Release();
  }

  return hres;
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Writing an Instance Provider</a>