---
UID: NF:wbemprov.IWbemHiPerfProvider.GetObjects
title: IWbemHiPerfProvider::GetObjects (wbemprov.h)
description: Inserts the non-key properties of the objects in the supplied array.
helpviewer_keywords: ["GetObjects","GetObjects method [Windows Management Instrumentation]","GetObjects method [Windows Management Instrumentation]","IWbemHiPerfProvider interface","IWbemHiPerfProvider interface [Windows Management Instrumentation]","GetObjects method","IWbemHiPerfProvider.GetObjects","IWbemHiPerfProvider::GetObjects","_hmm_iwbemhiperfprovider_getobjects","wbemprov/IWbemHiPerfProvider::GetObjects","wmi.iwbemhiperfprovider_getobjects"]
old-location: wmi\iwbemhiperfprovider_getobjects.htm
tech.root: wmi
ms.assetid: ba56b029-95d4-4c79-8385-0a5adb9f7dcc
ms.date: 12/05/2018
ms.keywords: GetObjects, GetObjects method [Windows Management Instrumentation], GetObjects method [Windows Management Instrumentation],IWbemHiPerfProvider interface, IWbemHiPerfProvider interface [Windows Management Instrumentation],GetObjects method, IWbemHiPerfProvider.GetObjects, IWbemHiPerfProvider::GetObjects, _hmm_iwbemhiperfprovider_getobjects, wbemprov/IWbemHiPerfProvider::GetObjects, wmi.iwbemhiperfprovider_getobjects
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
 - IWbemHiPerfProvider::GetObjects
 - wbemprov/IWbemHiPerfProvider::GetObjects
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
 - IWbemHiPerfProvider.GetObjects
---

# IWbemHiPerfProvider::GetObjects


## -description

The 
<b>IWbemHiPerfProvider::GetObjects</b> method inserts the non-key properties of the objects in the supplied array. WMI calls 
<b>GetObjects</b> in response to a 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a> call. If a provider does not implement 
<b>GetObjects</b>, WMI attempts to service a 
<b>GetObject</b> request with a call to the 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject">IWbemHiPerfProvider::CreateRefreshableObject</a> method.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.</div><div> </div>

## -parameters

### -param pNamespace [in]

An 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. The provider should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on this pointer if it is going to call back into Windows Management during its execution.

### -param lNumObjects [in]

Integer that contains the number of objects you are retrieving.

### -param apObj [in, out]

Pointer to an array of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a> objects. The <b>GetObjects</b> method inserts the key properties of each object into this array.

### -param lFlags

Reserved. This parameter must be 0.

### -param pContext

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in specific provider documentation. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI.</a>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

The requested objects will have their key properties filled out.


#### Examples

The following code example describes how to implement 
<b>GetObjects</b>.


```cpp
HRESULT CMyHiPerfProvider::GetObjects(
  /* [in] */IWbemServices *pNamespace,
  /* [in] */  long lNumObjects,
  /* [in,out] */IWbemObjectAccess **apObj,
  /* [in] */long lFlags,
  /* [in] */IWbemContext *pCtx
)
{

  for ( long i = 0; i < lNumObjects; i++ )
  {
      // Validate the instance (that is, ensure
      // the path is good); if it fails, return
      // the error.

      // For example, create a method that validates
      // the IWbemObjectAccess instance and returns
      // false if validation failed.
      /*if ( !ValidateInstance( apObj[i] ) )
          return WBEM_E_NOT_FOUND;*/

      // Fill out the instance.
      // For example, create a method that assigns
      // a value to the IWbemObjectAccess instance.
      /*FillInstance( apObj[i] );*/
  }

  return WBEM_S_NO_ERROR;
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Writing an Instance Provider</a>