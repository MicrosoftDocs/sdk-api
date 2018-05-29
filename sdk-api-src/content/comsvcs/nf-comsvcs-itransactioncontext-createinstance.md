---
UID: NF:comsvcs.ITransactionContext.CreateInstance
title: ITransactionContext::CreateInstance
author: windows-sdk-content
description: Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object.
old-location: cos\itransactioncontext_createinstance.htm
old-project: cossdk
ms.assetid: 3dc08700-0872-4d60-a968-cffed974c7b2
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: CreateInstance, CreateInstance method [COM+], CreateInstance method [COM+],ITransactionContext interface, ITransactionContext interface [COM+],CreateInstance method, ITransactionContext.CreateInstance, ITransactionContext::CreateInstance, _cos_ITransactionContext_CreateInstance, comsvcs/ITransactionContext::CreateInstance, cos.itransactioncontext_createinstance
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ITransactionContext.CreateInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionContext::CreateInstance


## -description


Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object.


## -parameters




### -param pszProgId [in]

A reference to the ProgID of the type of object to be instantiated.


### -param pObject [out]

A reference to the new object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



If the Microsoft Distributed Transaction Coordinator is not running and the object is transactional, the object is successfully created. However, method calls to that object will fail with CONTEXT_E_TMNOTAVAILABLE. Objects cannot recover from this condition and should be released.





## -see-also




<a href="https://msdn.microsoft.com/818fe18b-04ed-4f54-aeb7-b19aafc8a51a">ITransactionContext</a>
 

 

