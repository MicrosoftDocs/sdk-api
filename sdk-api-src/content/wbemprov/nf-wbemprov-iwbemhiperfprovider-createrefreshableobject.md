---
UID: NF:wbemprov.IWbemHiPerfProvider.CreateRefreshableObject
title: IWbemHiPerfProvider::CreateRefreshableObject (wbemprov.h)
description: Requests a refreshable instance object.
helpviewer_keywords: ["CreateRefreshableObject","CreateRefreshableObject method [Windows Management Instrumentation]","CreateRefreshableObject method [Windows Management Instrumentation]","IWbemHiPerfProvider interface","IWbemHiPerfProvider interface [Windows Management Instrumentation]","CreateRefreshableObject method","IWbemHiPerfProvider.CreateRefreshableObject","IWbemHiPerfProvider::CreateRefreshableObject","_hmm_iwbemhiperfprovider_createrefreshableobject","wbemprov/IWbemHiPerfProvider::CreateRefreshableObject","wmi.iwbemhiperfprovider_createrefreshableobject"]
old-location: wmi\iwbemhiperfprovider_createrefreshableobject.htm
tech.root: wmi
ms.assetid: 1eb414e0-cdf6-4caa-88a5-8da17a32449c
ms.date: 12/05/2018
ms.keywords: CreateRefreshableObject, CreateRefreshableObject method [Windows Management Instrumentation], CreateRefreshableObject method [Windows Management Instrumentation],IWbemHiPerfProvider interface, IWbemHiPerfProvider interface [Windows Management Instrumentation],CreateRefreshableObject method, IWbemHiPerfProvider.CreateRefreshableObject, IWbemHiPerfProvider::CreateRefreshableObject, _hmm_iwbemhiperfprovider_createrefreshableobject, wbemprov/IWbemHiPerfProvider::CreateRefreshableObject, wmi.iwbemhiperfprovider_createrefreshableobject
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
 - IWbemHiPerfProvider::CreateRefreshableObject
 - wbemprov/IWbemHiPerfProvider::CreateRefreshableObject
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
 - IWbemHiPerfProvider.CreateRefreshableObject
---

# IWbemHiPerfProvider::CreateRefreshableObject


## -description

The 
<b>IWbemHiPerfProvider::CreateRefreshableObject</b> method requests a refreshable instance object. The WMI Refresher calls <b>IWbemHiPerfProvider::CreateRefreshableObject</b> in response to a client request to the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath">IWbemConfigureRefresher::AddObjectByPath</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbytemplate">IWbemConfigureRefresher::AddObjectByTemplate</a> interfaces. The provider reads the key from the supplied template object and supplies an object in the <i>ppRefreshable</i> parameter that will be refreshed whenever the refresh method on <i>pRefresher</i> is called. The provider associates the refreshable object with the supplied refresher, obtained from an earlier call to 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher">IWbemHiPerfProvider::CreateRefresher</a>.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.</div><div> </div>

## -parameters

### -param pNamespace [in]

An 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. If the pointer must call back into WMI during its execution, the provider calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on it.

### -param pTemplate [in]

Pointer to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a> object that contains the template.

### -param pRefresher [in]

Pointer to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a> object that contains a refresher obtained by calling 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher">IWbemHiPerfProvider::CreateRefresher</a>.

### -param lFlags [in]

Reserved. This parameter must be 0.

### -param pContext [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the specific provider documentation. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppRefreshable [out]

Pointer that holds the reference to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a> object, which will contain the refreshable object.

### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies this refreshable object.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

The supplied instance template will contain an object with the key properties filled out. The returned object should be a unique, refreshable object. The provider must not touch the refreshable object except during a refresh operation. Your provider must not access the returned object, unless the object owning the refresher restores the object. The key properties of the supplied instance template will be filled out. The provider should also validate the instance path.


#### Examples

The following code example describes how to implement 
<b>CreateRefreshableObject</b>.


```cpp
HRESULT CMyHiPerfProvider::CreateRefreshableObject(
  /* [in] */IWbemServices *pNamespace,
  /* [in] */IWbemObjectAccess *pTemplate,
  /* [in] */IWbemRefresher *pRefresher,
  /* [in] */long lFlags,
  /* [in] */IWbemContext *pCtx,
  /* [out] */IWbemObjectAccess **ppRefreshable,
  /* [out] */ long *plId
)
{
  // Use a private interface defined
  // to talk with the refresher. You must define
  // the IMyRefresher interface.
  IMyRefresher* pMyRefr = NULL;

  HRESULT hres = pRefresher->QueryInterface(
    IID_IMyRefresher,
    (void**) &pMyRefr );

  if ( SUCCEEDED( hres ) )
  {
    // Check for a valid instance.
    // You must implement the ValidateInst function.
    if ( ValidateInst( pTemplate ) )
    {
      IWbemClassObject* pTemplateObj = NULL;
      IWbemClassObject* pCloneObj = NULL;
      IWbemObjectAccess* pCloneAcc = NULL;

      // Clone the object, then get an
      // IWbemObjectAccess pointer.
      pTemplate->QueryInterface(
        IID_IWbemClassObject,
        (void**) &pTemplateObj );

      pTemplateObj->Clone( &pCloneObj );

      pCloneObj->QueryInterface(
        IID_IWbemObjectAccess,
        (void**) &pCloneAcc );

      // Generate a unique identifier.
      // For example, use:
      /**plId = InterlockedIncrement( &m_lLastId );*/

      // Add the object to an array of
      // objects to refresh.
      //For example, use:
      /*pMyRefr->AddInstance( *plId, pCloneAcc );*/

      // Maintains AddRef from QI
      *ppRefreshable = pCloneAcc;

      pTemplateObj->Release();
      pCloneObj->Release();
    }
    else
    {
      hres = WBEM_E_NOT_FOUND;
    }

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