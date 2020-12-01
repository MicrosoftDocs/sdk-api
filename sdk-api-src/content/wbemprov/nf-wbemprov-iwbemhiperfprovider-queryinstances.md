---
UID: NF:wbemprov.IWbemHiPerfProvider.QueryInstances
title: IWbemHiPerfProvider::QueryInstances (wbemprov.h)
description: Returns instances of the specified class using the supplied IWbemObjectSink instance.
helpviewer_keywords: ["IWbemHiPerfProvider interface [Windows Management Instrumentation]","QueryInstances method","IWbemHiPerfProvider.QueryInstances","IWbemHiPerfProvider::QueryInstances","QueryInstances","QueryInstances method [Windows Management Instrumentation]","QueryInstances method [Windows Management Instrumentation]","IWbemHiPerfProvider interface","_hmm_iwbemhiperfprovider_queryinstances","wbemprov/IWbemHiPerfProvider::QueryInstances","wmi.iwbemhiperfprovider_queryinstances"]
old-location: wmi\iwbemhiperfprovider_queryinstances.htm
tech.root: wmi
ms.assetid: 8962fe9d-4b3e-469b-83e7-9c3f62a24308
ms.date: 12/05/2018
ms.keywords: IWbemHiPerfProvider interface [Windows Management Instrumentation],QueryInstances method, IWbemHiPerfProvider.QueryInstances, IWbemHiPerfProvider::QueryInstances, QueryInstances, QueryInstances method [Windows Management Instrumentation], QueryInstances method [Windows Management Instrumentation],IWbemHiPerfProvider interface, _hmm_iwbemhiperfprovider_queryinstances, wbemprov/IWbemHiPerfProvider::QueryInstances, wmi.iwbemhiperfprovider_queryinstances
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
 - IWbemHiPerfProvider::QueryInstances
 - wbemprov/IWbemHiPerfProvider::QueryInstances
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
 - IWbemHiPerfProvider.QueryInstances
---

# IWbemHiPerfProvider::QueryInstances


## -description

The 
<b>IWbemHiPerfProvider::QueryInstances</b> method returns instances of the specified class using the supplied 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> instance. The method should return immediately. The <a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> interface is used to specify results.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.</div><div> </div>

## -parameters

### -param pNamespace [in]

An 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer back to WMI that can service any request from the provider. The provider should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on this pointer if it  needs to call back to WMI during  execution.

### -param wszClass [in]

Pointer to a <b>WCHAR</b> string that specifies the class whose instances are returned.

### -param lFlags [in]

Integer that contains the flags.

### -param pCtx [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the  provider documentation. For more information, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pSink [in]

Pointer to the 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> implementation that is provided by the client to any of the asynchronous methods of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

HiPerf providers can report success or failure either through the return code from 
<b>QueryInstances</b> or through a call to the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> method of <i>pResponseHandler</i>. If you call the 
<b>SetStatus</b> method, the return code sent through <i>pResponseHandler</i> takes precedence over the 
<b>QueryInstances</b> return code.

## -remarks

WMI calls 
<b>QueryInstances</b> in response to an 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">IWbemServices::CreateInstanceEnum</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync">IWbemServices::CreateInstanceEnumAsync</a> request.

The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set. When error conditions occur, 
<b>IWbemObjectSink::SetStatus</b> may also be called with no intervening calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a>.


#### Examples

The following code example shows how to implement 
<b>QueryInstances</b>.


```cpp
HRESULT CMyHiPerfProvider::QueryInstances(
    /* [in] */ IWbemServices* pNamespace,  
    /* [in] */ BSTR strClass,
    /* [in] */ long lFlags,
    /* [in] */ IWbemContext __RPC_FAR *pCtx,
    /* [in] */ IWbemObjectSink __RPC_FAR *pSink
)
{
   IWbemClassObject *pClass = 0;
   IWbemClassObject *pNextInst = 0;

   // The IWbemObjectSink interface must be
   // implemented in a class that you define. You then
   // must assign the pResponseHandler pointer
   // an instance of the class that implements
   // the IWbemObjectSink interface.
   IWbemObjectSink* pResponseHandler = 0;
   HRESULT hRes;

    // Use the namespace pointer to retrieve a class
    // definition.

   hRes = pNamespace ->GetObject(strClass, 0, NULL, &pClass, 0);
   if (WBEM_NO_ERROR==hRes)
       return hRes;


    // Now loop through the private source and create each instance.

     for (int i = 0 ; i < NUM_OF_INSTANCES ; i++)
    {
         hRes = pClass->SpawnInstance(0, &pNextInst);

         // Exit loop if no new instance is spawned
         if (WBEM_S_FALSE == hRes)
            break;

        if(NULL!=pNextInst)
       {
        // Create the instance.
        // For example, call a function (FillInst) that
        // assigns a value to the pNextInst pointer.
        /*FillInst(pNextInst);*/

        // Deliver the class to WMI.
        pResponseHandler->Indicate(1, &pNextInst);
        pNextInst->Release(); 
        pNextInst=NULL;
       }
    }

   // Send a finish message to WMI.
    pResponseHandler->SetStatus(0, WBEM_S_NO_ERROR, 0, 0);
    // Free memory resources.
    pNamespace->Release();
    pClass->Release();
    SysFreeString(strClass);

  return WBEM_S_NO_ERROR;
}

```

## -see-also

<a href="/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Writing an Instance Provider</a>