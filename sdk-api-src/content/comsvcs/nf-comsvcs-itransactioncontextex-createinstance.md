---
UID: NF:comsvcs.ITransactionContextEx.CreateInstance
title: ITransactionContextEx::CreateInstance
author: windows-sdk-content
description: Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object.
old-location: cos\itransactioncontextex_createinstance.htm
tech.root: cossdk
ms.assetid: 49684f80-847b-4613-9148-dd34dc22a476
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateInstance, CreateInstance method [COM+], CreateInstance method [COM+],ITransactionContextEx interface, ITransactionContextEx interface [COM+],CreateInstance method, ITransactionContextEx.CreateInstance, ITransactionContextEx::CreateInstance, _cos_ITransactionContextEx_CreateInstance, comsvcs/ITransactionContextEx::CreateInstance, cos.itransactioncontextex_createinstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ITransactionContextEx.CreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransactionContextEx::CreateInstance


## -description


Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object.


## -parameters




### -param rclsid [in]

A reference to the CLSID of the type of object to be instantiated.


### -param riid [in]

A reference to the interface ID of the interface through which you will communicate with the new object.


### -param pObject [out]

A reference to a new object of the type specified by the <i>rclsid</i> parameter, through the interface specified by the <i>riid</i> parameter.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The component specified by <i>rclsid</i> is not registered as a COM component.


</td>
</tr>
</table>
 




## -remarks



If the Microsoft Distributed Transaction Coordinator is not running and the object is transactional, the object is successfully created. However, method calls to that object will fail with CONTEXT_E_TMNOTAVAILABLE. Objects cannot recover from this condition and should be released.



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ITransactionContextEx* pTransactionContext = NULL;
IMyObject* pMyObject = NULL;
HRESULT hr;

// Get TransactionContextEx.
hr = CoCreateInstance(CLSID_TransactionContextEx, 
  NULL, CLSCTX_INPROC, IID_ITransactionContextEx, 
  (void**)&amp;pTransactionContext);
if (FAILED(hr)) throw(hr);

// Create an instance of MyObject.
hr = pTransactionContext-&gt;CreateInstance(CLSID_CMyObject, 
  IID_IMyObject, (void**)&amp;pMyObject);
if (FAILED(hr)) throw(hr);

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cdf3a74f-cdef-4721-9c0d-90af724c24ba">ITransactionContextEx</a>
 

 

