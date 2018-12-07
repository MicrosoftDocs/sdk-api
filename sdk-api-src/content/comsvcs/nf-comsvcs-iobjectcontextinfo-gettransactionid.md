---
UID: NF:comsvcs.IObjectContextInfo.GetTransactionId
title: IObjectContextInfo::GetTransactionId
author: windows-sdk-content
description: Retrieves the identifier of the current transaction.
old-location: cos\iobjectcontextinfo_gettransactionid.htm
tech.root: cossdk
ms.assetid: c8aa6fe8-acb2-4e00-a7fc-605bb56969e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTransactionId, GetTransactionId method [COM+], GetTransactionId method [COM+],IObjectContextInfo interface, IObjectContextInfo interface [COM+],GetTransactionId method, IObjectContextInfo.GetTransactionId, IObjectContextInfo::GetTransactionId, _cos_IObjectContextInfo_GetTransactionId, comsvcs/IObjectContextInfo::GetTransactionId, cos.iobjectcontextinfo_gettransactionid
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
 - IObjectContextInfo.GetTransactionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectContextInfo::GetTransactionId


## -description


Retrieves the identifier of the current transaction.


## -parameters




### -param pGuid [out]

A GUID that identifies the current transaction.


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
The method completed succesfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object is not executing in a transaction.

</td>
</tr>
</table>
 




## -remarks



Objects in the same transaction share the same transaction identifier.




## -see-also




<a href="https://msdn.microsoft.com/76dcc6f3-f840-4672-bba9-038c1249a306">IObjectContextInfo</a>
 

 

