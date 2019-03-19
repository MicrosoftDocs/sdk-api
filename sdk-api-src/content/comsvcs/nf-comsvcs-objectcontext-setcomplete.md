---
UID: NF:comsvcs.ObjectContext.SetComplete
title: ObjectContext::SetComplete (comsvcs.h)
author: windows-sdk-content
description: Declares that the transaction in which the object is executing can be committed and that the object should be deactivated on return.
old-location: cos\objectcontext_setcomplete.htm
tech.root: cossdk
ms.assetid: 3bf3bbc2-9b4f-4dba-89ef-62c58640710b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ObjectContext interface [COM+],SetComplete method, ObjectContext.SetComplete, ObjectContext::SetComplete, SetComplete, SetComplete method [COM+], SetComplete method [COM+],ObjectContext interface, _cos_ObjectContext_SetComplete, comsvcs/ObjectContext::SetComplete, cos.objectcontext_setcomplete
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
 - ObjectContext.SetComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ObjectContext::SetComplete


## -description


Declares that the transaction in which the object is executing can be committed and that the object should be deactivated on return.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred. This can happen if one object passes its <a href="https://msdn.microsoft.com/en-us/library/ms678909(v=VS.85).aspx">ObjectContext</a> pointer to another object and the other object calls <a href="https://msdn.microsoft.com/3bf3bbc2-9b4f-4dba-89ef-62c58640710b">SetComplete</a> using this pointer. An <b>ObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>
 




## -remarks



The object is deactivated automatically on return from the method in which it called <b>SetComplete</b>. If the object is the root of an automatic transaction, COM+ attempts to commit the transaction. However, if any object that was participating in the transaction has called <a href="https://msdn.microsoft.com/709c1752-f2fb-463e-a95e-a082cd28b110">SetAbort</a>, or has called <a href="https://msdn.microsoft.com/cf0e59d9-2760-445e-aa7d-8c2b78457181">DisableCommit</a> and has not subsequently called <a href="https://msdn.microsoft.com/c625d3e2-8a12-4049-8997-6e57c3423acc">EnableCommit</a> or <b>SetComplete</b>, the transaction is aborted.

If an object does not need to maintain its state after it returns from a method call, it should call <b>SetComplete</b> so that it can be automatically deactivated as soon as it returns and its resources can be reclaimed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms678909(v=VS.85).aspx">ObjectContext</a>
 

 

