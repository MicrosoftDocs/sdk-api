---
UID: NF:comsvcs.ContextInfo.GetTransaction
title: ContextInfo::GetTransaction
author: windows-sdk-content
description: Retrieves the object context's transaction object.
old-location: cos\contextinfo_gettransaction.htm
tech.root: cossdk
ms.assetid: 9922f2a3-9b2e-4bfe-8a9a-a17c0628439e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ContextInfo interface [COM+],GetTransaction method, ContextInfo.GetTransaction, ContextInfo::GetTransaction, GetTransaction, GetTransaction method [COM+], GetTransaction method [COM+],ContextInfo interface, _cos_ContextInfo_GetTransaction, comsvcs/ContextInfo::GetTransaction, cos.contextinfo_gettransaction
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
 - ContextInfo.GetTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ContextInfo::GetTransaction


## -description


Retrieves the object context's transaction object.


## -parameters




### -param ppTx [out]

A reference to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the transaction object for the currently executing transaction.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object is not executing in a transaction. The <i>ppTx</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ef8d7ef7-fae4-4a20-80fb-18f5daa9b564">ContextInfo</a>
 

 

