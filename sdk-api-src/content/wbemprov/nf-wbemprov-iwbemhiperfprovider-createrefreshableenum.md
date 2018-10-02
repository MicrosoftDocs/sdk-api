---
UID: NF:wbemprov.IWbemHiPerfProvider.CreateRefreshableEnum
title: IWbemHiPerfProvider::CreateRefreshableEnum
author: windows-sdk-content
description: Creates a new refreshable enumeration.
old-location: wmi\iwbemhiperfprovider_createrefreshableenum.htm
tech.root: WmiSdk
ms.assetid: 086a1717-b6e8-45c1-9397-ec894ee900a0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateRefreshableEnum, CreateRefreshableEnum method [Windows Management Instrumentation], CreateRefreshableEnum method [Windows Management Instrumentation],IWbemHiPerfProvider interface, IWbemHiPerfProvider interface [Windows Management Instrumentation],CreateRefreshableEnum method, IWbemHiPerfProvider.CreateRefreshableEnum, IWbemHiPerfProvider::CreateRefreshableEnum, _hmm_iwbemhiperfprovider_createrefreshableenum, wbemprov/IWbemHiPerfProvider::CreateRefreshableEnum, wmi.iwbemhiperfprovider_createrefreshableenum
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
req.lib: Wbemuuid.lib
req.dll: Wmiprvsd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiprvsd.dll
api_name:
 - IWbemHiPerfProvider.CreateRefreshableEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemHiPerfProvider::CreateRefreshableEnum


## -description


The 
<b>IWbemHiPerfProvider::CreateRefreshableEnum</b> method creates a new refreshable enumeration. The WMI Refresher calls this method in response to a client request to 
<a href="https://msdn.microsoft.com/5b013267-78bc-4372-b55a-58e330acf927">IWbemConfigureRefresher::AddEnum</a>. The provider associates the supplied 
<a href="https://msdn.microsoft.com/71ce1c89-446e-4137-9857-9d3c5921e0b7">IWbemHiPerfEnum</a> object with the supplied refresher. On each call to the supplied refresher's 
<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">Refresh</a> method, the provider ensures that the enumerator contains a set of all the instances of the class listed in the <i>wszClass</i> parameter and that these instances contain updated information. One possible way to do this would be to keep an array of refreshable enumerators in the refresher.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.</div><div> </div>

## -parameters




### -param pNamespace [in]

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back into Windows Management, which can service any requests made by the provider. If <i>pNamespace</i> must call back into Windows Management during its execution, the provider calls <a href="_com_iunknown_addref">AddRef</a> on this pointer.


### -param wszClass [in]

Constant, <b>null</b>-terminated string of 16-bit, Unicode characters that contains the name of the class, whose instances are refreshed in the <i>pHiPerfEnum </i> parameter.


### -param pRefresher [in]

Pointer to a 
<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a> object that contains a refresher obtained by calling 
<a href="https://msdn.microsoft.com/5962f5f6-a121-4234-8dcd-24c0e2b53990">IWbemHiPerfProvider::CreateRefresher</a>.


### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param pContext

TBD


### -param pHiPerfEnum [in]

Pointer to a 
<a href="https://msdn.microsoft.com/71ce1c89-446e-4137-9857-9d3c5921e0b7">IWbemHiPerfEnum</a> object that contains the high-performance enumeration.


### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies the refreshable enumeration.


#### - pCtx [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object required by one or more dynamic class providers. The values in the context object must be specified in the specific provider's documentation. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The provider must not modify the refreshable enumerator except during a refresh operation. The enumeration is shallow, so all instances placed in the enumerator should be of the class specified by <i>wszClass</i>.

The provider must not access the enumerator unless WMI calls the 
<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">IWbemRefresher::Refresh</a> method of the owner. As with refreshable objects, the provider must not update the enumerator unless the object owning the enumerator refreshes the enumerator.


#### Examples

The following code example describes how to implement 
<b>CreateRefreshableEnum</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CHiPerfProvider::CreateRefreshableEnum(
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

  HRESULT hres = pRefresher-&gt;QueryInterface(
    IID_IMyRefresher,
    (void**) &amp;pMyRefr );

  if ( SUCCEEDED( hres ) )
  {
  LPLONG plLastId;
    // Generates a unique identifier
    *plId = InterlockedIncrement( &amp;plLastId );

    // Use an internal method to add the
    // enumerator to an array.
    pMyRefr-&gt;AddEnum( wszClass, *plId, pEnum );

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
 

 

