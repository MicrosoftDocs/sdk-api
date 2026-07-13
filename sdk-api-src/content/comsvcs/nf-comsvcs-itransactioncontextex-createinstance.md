---
UID: NF:comsvcs.ITransactionContextEx.CreateInstance
title: ITransactionContextEx::CreateInstance (comsvcs.h)
description: Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object. (ITransactionContextEx.CreateInstance)
helpviewer_keywords: ["CreateInstance","CreateInstance method [COM+]","CreateInstance method [COM+]","ITransactionContextEx interface","ITransactionContextEx interface [COM+]","CreateInstance method","ITransactionContextEx.CreateInstance","ITransactionContextEx::CreateInstance","_cos_ITransactionContextEx_CreateInstance","comsvcs/ITransactionContextEx::CreateInstance","cos.itransactioncontextex_createinstance"]
old-location: cos\itransactioncontextex_createinstance.htm
tech.root: cos
ms.assetid: 49684f80-847b-4613-9148-dd34dc22a476
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [COM+], CreateInstance method [COM+],ITransactionContextEx interface, ITransactionContextEx interface [COM+],CreateInstance method, ITransactionContextEx.CreateInstance, ITransactionContextEx::CreateInstance, _cos_ITransactionContextEx_CreateInstance, comsvcs/ITransactionContextEx::CreateInstance, cos.itransactioncontextex_createinstance
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITransactionContextEx::CreateInstance
 - comsvcs/ITransactionContextEx::CreateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ITransactionContextEx.CreateInstance
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


```cpp
ITransactionContextEx* pTransactionContext = NULL;
IMyObject* pMyObject = NULL;
HRESULT hr;

// Get TransactionContextEx.
hr = CoCreateInstance(CLSID_TransactionContextEx, 
  NULL, CLSCTX_INPROC, IID_ITransactionContextEx, 
  (void**)&pTransactionContext);
if (FAILED(hr)) throw(hr);

// Create an instance of MyObject.
hr = pTransactionContext->CreateInstance(CLSID_CMyObject, 
  IID_IMyObject, (void**)&pMyObject);
if (FAILED(hr)) throw(hr);


```

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontextex">ITransactionContextEx</a>
