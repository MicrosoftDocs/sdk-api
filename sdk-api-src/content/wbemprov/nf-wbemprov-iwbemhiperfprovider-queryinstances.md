---
UID: NF:wbemprov.IWbemHiPerfProvider.QueryInstances
title: IWbemHiPerfProvider::QueryInstances
author: windows-sdk-content
description: Returns instances of the specified class using the supplied IWbemObjectSink instance.
old-location: wmi\iwbemhiperfprovider_queryinstances.htm
old-project: WmiSdk
ms.assetid: 8962fe9d-4b3e-469b-83e7-9c3f62a24308
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IWbemHiPerfProvider interface [Windows Management Instrumentation],QueryInstances method, IWbemHiPerfProvider.QueryInstances, IWbemHiPerfProvider::QueryInstances, QueryInstances, QueryInstances method [Windows Management Instrumentation], QueryInstances method [Windows Management Instrumentation],IWbemHiPerfProvider interface, _hmm_iwbemhiperfprovider_queryinstances, wbemprov/IWbemHiPerfProvider::QueryInstances, wmi.iwbemhiperfprovider_queryinstances
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiprvsd.dll
api_name:
 - IWbemHiPerfProvider.QueryInstances
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemHiPerfProvider::QueryInstances


## -description


The 
<b>IWbemHiPerfProvider::QueryInstances</b> method returns instances of the specified class using the supplied 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> instance. The method should return immediately. The <a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> interface is used to specify results.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.</div><div> </div>

## -parameters




### -param pNamespace [in]

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back to WMI that can service any request from the provider. The provider should call <a href="https://msdn.microsoft.com/library/Dd757100(v=VS.85).aspx">AddRef</a> on this pointer if it  needs to call back to WMI during  execution.


### -param wszClass [in]

Pointer to a <b>WCHAR</b> string that specifies the class whose instances are returned.


### -param lFlags [in]

Integer that contains the flags.


### -param pCtx [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the  provider documentation. For more information, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param pSink [in]

Pointer to the 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> implementation that is provided by the client to any of the asynchronous methods of 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

HiPerf providers can report success or failure either through the return code from 
<b>QueryInstances</b> or through a call to the 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> method of <i>pResponseHandler</i>. If you call the 
<b>SetStatus</b> method, the return code sent through <i>pResponseHandler</i> takes precedence over the 
<b>QueryInstances</b> return code.




## -remarks



WMI calls 
<b>QueryInstances</b> in response to an 
<a href="https://msdn.microsoft.com/47671b9b-a2ff-4375-b2a4-7e8599f1fb69">IWbemServices::CreateInstanceEnum</a> or 
<a href="https://msdn.microsoft.com/5ba2ff28-034f-4949-9bde-8c98345ec7c6">IWbemServices::CreateInstanceEnumAsync</a> request.

The 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set. When error conditions occur, 
<b>IWbemObjectSink::SetStatus</b> may also be called with no intervening calls to 
<a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">IWbemObjectSink::Indicate</a>.


#### Examples

The following code example shows how to implement 
<b>QueryInstances</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CMyHiPerfProvider::QueryInstances(
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

   hRes = pNamespace -&gt;GetObject(strClass, 0, NULL, &amp;pClass, 0);
   if (WBEM_NO_ERROR==hRes)
       return hRes;


    // Now loop through the private source and create each instance.

     for (int i = 0 ; i &lt; NUM_OF_INSTANCES ; i++)
    {
         hRes = pClass-&gt;SpawnInstance(0, &amp;pNextInst);

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
        pResponseHandler-&gt;Indicate(1, &amp;pNextInst);
        pNextInst-&gt;Release(); 
        pNextInst=NULL;
       }
    }

   // Send a finish message to WMI.
    pResponseHandler-&gt;SetStatus(0, WBEM_S_NO_ERROR, 0, 0);
    // Free memory resources.
    pNamespace-&gt;Release();
    pClass-&gt;Release();
    SysFreeString(strClass);

  return WBEM_S_NO_ERROR;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a4f537ba-9081-43b4-acff-4d206de3d9d7">Developing a WMI Provider</a>



<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Writing an Instance Provider</a>
 

 

