---
UID: NF:comsvcs.IObjectContextInfo.GetTransaction
title: IObjectContextInfo::GetTransaction (comsvcs.h)
author: windows-sdk-content
description: Retrieves a reference to the current transaction.
old-location: cos\iobjectcontextinfo_gettransaction.htm
tech.root: cossdk
ms.assetid: e3a19d49-740a-436c-be6b-c98b5a14dc93
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTransaction, GetTransaction method [COM+], GetTransaction method [COM+],IObjectContextInfo interface, IObjectContextInfo interface [COM+],GetTransaction method, IObjectContextInfo.GetTransaction, IObjectContextInfo::GetTransaction, _cos_IObjectContextInfo_GetTransaction, comsvcs/IObjectContextInfo::GetTransaction, cos.iobjectcontextinfo_gettransaction
ms.topic: method
f1_keywords: ["comsvcs/IObjectContextInfo.GetTransaction"]
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
ms.custom: 19H1
---

# IObjectContextInfo::GetTransaction


## -description


Retrieves a reference to the current transaction. You can use this reference to manually enlist a resource manager that does not support automatic transactions.


## -parameters




### -param pptrans [out]

A reference to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the transaction that is currently executing. You can then <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> to get the <b>ITransaction</b> interface for the current transaction.


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




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a>
 

 

