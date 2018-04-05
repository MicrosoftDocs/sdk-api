---
UID: NF:comsvcs.ITransactionProperty.GetTransactionResourcePool
title: ITransactionProperty::GetTransactionResourcePool method
author: windows-driver-content
description: Retrieves the resource pool that is associated with this context's transaction.
old-location: cos\itransactionproperty_gettransactionresourcepool.htm
old-project: cossdk
ms.assetid: 497cfbd8-122f-45c8-a34a-7e7df4932ad1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetTransactionResourcePool method [COM+], GetTransactionResourcePool method [COM+], ITransactionProperty interface, GetTransactionResourcePool,ITransactionProperty.GetTransactionResourcePool, ITransactionProperty, ITransactionProperty interface [COM+], GetTransactionResourcePool method, ITransactionProperty::GetTransactionResourcePool, _cos_ITransactionProperty_GetTransactionResourcePool, comsvcs/ITransactionProperty::GetTransactionResourcePool, cos.itransactionproperty_gettransactionresourcepool
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	ITransactionProperty.GetTransactionResourcePool
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionProperty::GetTransactionResourcePool method


## -description


Retrieves the resource pool that is associated with this context's transaction.


## -parameters




### -param ppTxPool [out]

A reference to the transaction resource pool.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/602842ce-abb1-4830-99b3-d361d18ac074">ITransactionProperty</a>



<a href="https://msdn.microsoft.com/bf7ca849-6025-4358-bf2d-629d80e06a04">ITransactionResourcePool</a>
 

 

