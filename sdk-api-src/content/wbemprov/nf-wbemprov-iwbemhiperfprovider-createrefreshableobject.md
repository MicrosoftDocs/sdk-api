---
UID: NF:wbemprov.IWbemHiPerfProvider.CreateRefreshableObject
title: IWbemHiPerfProvider::CreateRefreshableObject
author: windows-sdk-content
description: Requests a refreshable instance object.
old-location: wmi\iwbemhiperfprovider_createrefreshableobject.htm
old-project: WmiSdk
ms.assetid: 1eb414e0-cdf6-4caa-88a5-8da17a32449c
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: CreateRefreshableObject, CreateRefreshableObject method [Windows Management Instrumentation], CreateRefreshableObject method [Windows Management Instrumentation],IWbemHiPerfProvider interface, IWbemHiPerfProvider interface [Windows Management Instrumentation],CreateRefreshableObject method, IWbemHiPerfProvider.CreateRefreshableObject, IWbemHiPerfProvider::CreateRefreshableObject, _hmm_iwbemhiperfprovider_createrefreshableobject, wbemprov/IWbemHiPerfProvider::CreateRefreshableObject, wmi.iwbemhiperfprovider_createrefreshableobject
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
 - IWbemHiPerfProvider.CreateRefreshableObject
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemHiPerfProvider::CreateRefreshableObject


## -description


The 
<b>IWbemHiPerfProvider::CreateRefreshableObject</b> method requests a refreshable instance object. The WMI Refresher calls <b>IWbemHiPerfProvider::CreateRefreshableObject</b> in response to a client request to the 
<a href="https://msdn.microsoft.com/85721e0c-863b-45af-91ca-8ee14af37181">IWbemConfigureRefresher::AddObjectByPath</a> or 
<a href="https://msdn.microsoft.com/c3f25484-7c6c-4625-9d26-1c01d15b10c4">IWbemConfigureRefresher::AddObjectByTemplate</a> interfaces. The provider reads the key from the supplied template object and supplies an object in the <i>ppRefreshable</i> parameter that will be refreshed whenever the refresh method on <i>pRefresher</i> is called. The provider associates the refreshable object with the supplied refresher, obtained from an earlier call to 
<a href="https://msdn.microsoft.com/5962f5f6-a121-4234-8dcd-24c0e2b53990">IWbemHiPerfProvider::CreateRefresher</a>.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.</div><div> </div>

## -parameters




### -param pNamespace [in]

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. If the pointer must call back into WMI during its execution, the provider calls <a href="https://msdn.microsoft.com/library/ms691379(v=VS.85).aspx">AddRef</a> on it.


### -param pTemplate [in]

Pointer to a 
<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a> object that contains the template.


### -param pRefresher [in]

Pointer to a 
<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a> object that contains a refresher obtained by calling 
<a href="https://msdn.microsoft.com/5962f5f6-a121-4234-8dcd-24c0e2b53990">IWbemHiPerfProvider::CreateRefresher</a>.


### -param lFlags [in]

Reserved. This parameter must be 0.


### -param pContext




### -param ppRefreshable [out]

Pointer that holds the reference to a 
<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a> object, which will contain the refreshable object.


### -param plId






#### - pCtx [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the specific provider documentation. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


#### - pLid [out]

Pointer to an integer returned by the provider that uniquely identifies this refreshable object.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The supplied instance template will contain an object with the key properties filled out. The returned object should be a unique, refreshable object. The provider must not touch the refreshable object except during a refresh operation. Your provider must not access the returned object, unless the object owning the refresher restores the object. The key properties of the supplied instance template will be filled out. The provider should also validate the instance path.


#### Examples

The following code example describes how to implement 
<b>CreateRefreshableObject</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CMyHiPerfProvider::CreateRefreshableObject(
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

  HRESULT hres = pRefresher-&gt;QueryInterface(
    IID_IMyRefresher,
    (void**) &amp;pMyRefr );

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
      pTemplate-&gt;QueryInterface(
        IID_IWbemClassObject,
        (void**) &amp;pTemplateObj );

      pTemplateObj-&gt;Clone( &amp;pCloneObj );

      pCloneObj-&gt;QueryInterface(
        IID_IWbemObjectAccess,
        (void**) &amp;pCloneAcc );

      // Generate a unique identifier.
      // For example, use:
      /**plId = InterlockedIncrement( &amp;m_lLastId );*/

      // Add the object to an array of
      // objects to refresh.
      //For example, use:
      /*pMyRefr-&gt;AddInstance( *plId, pCloneAcc );*/

      // Maintains AddRef from QI
      *ppRefreshable = pCloneAcc;

      pTemplateObj-&gt;Release();
      pCloneObj-&gt;Release();
    }
    else
    {
      hres = WBEM_E_NOT_FOUND;
    }

    pMyRefr-&gt;Release();
  }

  return hres;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a4f537ba-9081-43b4-acff-4d206de3d9d7">Developing a WMI Provider</a>



<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Writing an Instance Provider</a>
 

 

