---
UID: NF:comsvcs.IObjectContextInfo.GetTransaction
title: IObjectContextInfo::GetTransaction
author: windows-sdk-content
description: Retrieves a reference to the current transaction.
old-location: cos\iobjectcontextinfo_gettransaction.htm
tech.root: cossdk
ms.assetid: e3a19d49-740a-436c-be6b-c98b5a14dc93
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetTransaction, GetTransaction method [COM+], GetTransaction method [COM+],IObjectContextInfo interface, IObjectContextInfo interface [COM+],GetTransaction method, IObjectContextInfo.GetTransaction, IObjectContextInfo::GetTransaction, _cos_IObjectContextInfo_GetTransaction, comsvcs/IObjectContextInfo::GetTransaction, cos.iobjectcontextinfo_gettransaction
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
 - IObjectContextInfo.GetTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectContextInfo::GetTransaction


## -description


Retrieves a reference to the current transaction. You can use this reference to manually enlist a resource manager that does not support automatic transactions.


## -parameters




### -param pptrans [out]

A reference to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the transaction that is currently executing. You can then <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to get the <b>ITransaction</b> interface for the current transaction.


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
The object is executing in a transaction.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object is not executing in a transaction. The <i>pptrans</i> parameter is <b>NULL</b>.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/76dcc6f3-f840-4672-bba9-038c1249a306">IObjectContextInfo</a>
 

 

