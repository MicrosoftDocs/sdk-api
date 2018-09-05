---
UID: NF:wbemprov.IWbemHiPerfProvider.GetObjects
title: IWbemHiPerfProvider::GetObjects
author: windows-sdk-content
description: Inserts the non-key properties of the objects in the supplied array.
old-location: wmi\iwbemhiperfprovider_getobjects.htm
old-project: WmiSdk
ms.assetid: ba56b029-95d4-4c79-8385-0a5adb9f7dcc
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: GetObjects, GetObjects method [Windows Management Instrumentation], GetObjects method [Windows Management Instrumentation],IWbemHiPerfProvider interface, IWbemHiPerfProvider interface [Windows Management Instrumentation],GetObjects method, IWbemHiPerfProvider.GetObjects, IWbemHiPerfProvider::GetObjects, _hmm_iwbemhiperfprovider_getobjects, wbemprov/IWbemHiPerfProvider::GetObjects, wmi.iwbemhiperfprovider_getobjects
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.redist: 
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
 - IWbemHiPerfProvider.GetObjects
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemHiPerfProvider::GetObjects


## -description


The 
<b>IWbemHiPerfProvider::GetObjects</b> method inserts the non-key properties of the objects in the supplied array. WMI calls 
<b>GetObjects</b> in response to a 
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a> call. If a provider does not implement 
<b>GetObjects</b>, WMI attempts to service a 
<b>GetObject</b> request with a call to the 
<a href="https://msdn.microsoft.com/1eb414e0-cdf6-4caa-88a5-8da17a32449c">IWbemHiPerfProvider::CreateRefreshableObject</a> method.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.</div><div> </div>

## -parameters




### -param pNamespace [in]

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. The provider should call <a href="_com_iunknown_addref">AddRef</a> on this pointer if it is going to call back into Windows Management during its execution.


### -param lNumObjects [in]

Integer that contains the number of objects you are retrieving.


### -param apObj [in, out]

Pointer to an array of 
<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a> objects. The <b>GetObjects</b> method inserts the key properties of each object into this array.


### -param lFlags

Reserved. This parameter must be 0.


### -param pContext






#### - pCtx

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in specific provider documentation. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI.</a>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The requested objects will have their key properties filled out.


#### Examples

The following code example describes how to implement 
<b>GetObjects</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CMyHiPerfProvider::GetObjects(
  /* [in] */IWbemServices *pNamespace,
  /* [in] */  long lNumObjects,
  /* [in,out] */IWbemObjectAccess **apObj,
  /* [in] */long lFlags,
  /* [in] */IWbemContext *pCtx
)
{

  for ( long i = 0; i &lt; lNumObjects; i++ )
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
 

 

