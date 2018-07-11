---
UID: NF:comsvcs.ITransactionResourcePool.PutResource
title: ITransactionResourcePool::PutResource
author: windows-sdk-content
description: Adds an object to the list of pooled objects.
old-location: cos\itransactionresourcepool_putresource.htm
old-project: cossdk
ms.assetid: 6e05f075-0fa8-4605-9f68-3ef7fc9f0132
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: ITransactionResourcePool interface [COM+],PutResource method, ITransactionResourcePool.PutResource, ITransactionResourcePool::PutResource, PutResource, PutResource method [COM+], PutResource method [COM+],ITransactionResourcePool interface, _cos_ITransactionResourcePool_PutResource, comsvcs/ITransactionResourcePool::PutResource, cos.itransactionresourcepool_putresource
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ITransactionResourcePool.PutResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionResourcePool::PutResource


## -description


Adds an object to the list of pooled objects.


## -parameters




### -param pPool [in]

The key to each object in the transaction resource pool. It determines the type of pooled object to add to the list.


### -param pUnk [in]

A reference to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the pooled object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/d3730a37-933b-4705-b787-4b8bb728a278">IObjPool</a>



<a href="https://msdn.microsoft.com/bf7ca849-6025-4358-bf2d-629d80e06a04">ITransactionResourcePool</a>
 

 

