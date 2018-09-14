---
UID: NF:comsvcs.ITransactionResourcePool.GetResource
title: ITransactionResourcePool::GetResource
author: windows-sdk-content
description: Retrieves an object from the list of pooled objects.
old-location: cos\itransactionresourcepool_getresource.htm
tech.root: cossdk
ms.assetid: 68e71746-e3a1-4f33-a3b8-fa8bf9608776
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetResource, GetResource method [COM+], GetResource method [COM+],ITransactionResourcePool interface, ITransactionResourcePool interface [COM+],GetResource method, ITransactionResourcePool.GetResource, ITransactionResourcePool::GetResource, _cos_ITransactionResourcePool_GetResource, comsvcs/ITransactionResourcePool::GetResource, cos.itransactionresourcepool_getresource
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
 - ITransactionResourcePool.GetResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransactionResourcePool::GetResource


## -description


Retrieves an object from the list of pooled objects.


## -parameters




### -param pPool [in]

The key to each object in the transaction resource pool. It determines the type of pooled object to retrieve from the list.


### -param ppUnk [out]

A reference to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the pooled object.

The object that is retrieved must have the same <a href="https://msdn.microsoft.com/d3730a37-933b-4705-b787-4b8bb728a278">IObjPool</a> pointer as an object that was put on the list by using <a href="https://msdn.microsoft.com/6e05f075-0fa8-4605-9f68-3ef7fc9f0132">PutResource</a>.



## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
<dt><b>E_FAILED </b></dt>
</dl>
</td>
<td width="60%">
The <i>pPool</i> parameter did not match any object on the list of pooled objects.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3730a37-933b-4705-b787-4b8bb728a278">IObjPool</a>



<a href="https://msdn.microsoft.com/bf7ca849-6025-4358-bf2d-629d80e06a04">ITransactionResourcePool</a>
 

 

