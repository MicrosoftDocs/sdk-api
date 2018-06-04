---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ObjectContext::EnableCommit


## -description


Declares that the current object's work is not necessarily finished but that its transactional updates are consistent and could be committed in their present form.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

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
The method completed succesfully and the object's transactional updates can now be committed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred. This can happen if one object passes its <a href="https://msdn.microsoft.com/09a17e57-7224-43bc-93c7-16ab95ca2517">ObjectContext</a> pointer to another object and the other object calls <a href="https://msdn.microsoft.com/c625d3e2-8a12-4049-8997-6e57c3423acc">EnableCommit</a> using this pointer. An <b>ObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>
 




## -remarks



When an object calls <b>EnableCommit</b>, it allows the transaction in which it's participating to be committed but it maintains its internal state across calls from its clients until it calls <a href="https://msdn.microsoft.com/3bf3bbc2-9b4f-4dba-89ef-62c58640710b">SetComplete</a> or <a href="https://msdn.microsoft.com/709c1752-f2fb-463e-a95e-a082cd28b110">SetAbort</a> or until the transaction completes.

<b>EnableCommit</b> is the default state when an object is activated. Therefore, an object should always call <a href="https://msdn.microsoft.com/3bf3bbc2-9b4f-4dba-89ef-62c58640710b">SetComplete</a> or <a href="https://msdn.microsoft.com/709c1752-f2fb-463e-a95e-a082cd28b110">SetAbort</a> before returning from a method, unless you want the object to maintain its internal state for the next call from a client.




## -see-also




<a href="https://msdn.microsoft.com/09a17e57-7224-43bc-93c7-16ab95ca2517">ObjectContext</a>
 

 

