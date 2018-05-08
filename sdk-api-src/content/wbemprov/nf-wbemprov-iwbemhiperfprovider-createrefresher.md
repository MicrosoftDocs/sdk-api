---
UID: NF:wbemprov.IWbemHiPerfProvider.CreateRefresher
title: IWbemHiPerfProvider::CreateRefresher
author: windows-driver-content
description: Creates a refresher.
old-location: wmi\iwbemhiperfprovider_createrefresher.htm
old-project: WmiSdk
ms.assetid: 5962f5f6-a121-4234-8dcd-24c0e2b53990
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: CreateRefresher, CreateRefresher method [Windows Management Instrumentation], CreateRefresher method [Windows Management Instrumentation],IWbemHiPerfProvider interface, IWbemHiPerfProvider interface [Windows Management Instrumentation],CreateRefresher method, IWbemHiPerfProvider.CreateRefresher, IWbemHiPerfProvider::CreateRefresher, _hmm_iwbemhiperfprovider_createrefresher, wbemprov/IWbemHiPerfProvider::CreateRefresher, wmi.iwbemhiperfprovider_createrefresher
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WbemTimeout
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmiprvsd.dll
api_name:
-	IWbemHiPerfProvider.CreateRefresher
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemHiPerfProvider::CreateRefresher


## -description


The 
<b>IWbemHiPerfProvider::CreateRefresher</b> method creates a refresher. The returned refresher will be used in subsequent calls to 
<a href="https://msdn.microsoft.com/086a1717-b6e8-45c1-9397-ec894ee900a0">IWbemHiPerfProvider::CreateRefreshableEnum</a>, 
<a href="https://msdn.microsoft.com/1eb414e0-cdf6-4caa-88a5-8da17a32449c">IWbemHiPerfProvider::CreateRefreshableObject</a>, and 
<a href="https://msdn.microsoft.com/d1de54de-b57b-4e15-84b3-96cc36bf023b">IWbemHiPerfProvider::StopRefreshing</a>.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>. A provider must implement this method to support refresher operations.</div><div> </div>

## -parameters




### -param pNamespace [in]

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. The provider should call <a href="_com_iunknown_addref">AddRef</a> on this pointer if it is going to call back into Windows Management during its execution.


### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param ppRefresher [out]

Pointer to hold the reference to the provider's implementation of the 
<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a> interface.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The provider must supply its own implementation of the 
<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a> interface. It is valid for WMI to request multiple refreshers, each of which will be used for its own refresh operations.

When you release a refresher, the provider should clean up any refreshable objects or enumerators that were added to the refresher.


#### Examples

The following code example describes how to implement 
<b>CreateRefresher</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CHiPerfProvider::CreateRefresher(
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
    /*return pMyRefresher-&gt;QueryInterface(
     IID_IWbemRefresher, (void**) ppRefresher );*/
}

// Free memory resources.
// For Example:
//pNamespace-&gt;Release();
//ppRefresher-&gt;Release();
//delete[] pMyRefresher;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a4f537ba-9081-43b4-acff-4d206de3d9d7">Developing a WMI Provider</a>



<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Writing an Instance Provider</a>
 

 

