---
UID: NF:comsvcs.IObjectContext.SetComplete
title: IObjectContext::SetComplete
author: windows-sdk-content
description: Declares that the transaction in which the object is executing can be committed and that the object should be deactivated when it returns from the currently executing method call.
old-location: cos\iobjectcontext_setcomplete.htm
old-project: cossdk
ms.assetid: 8ff25b68-fcb3-4e11-9c74-b49b31806796
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IObjectContext interface [COM+],SetComplete method, IObjectContext.SetComplete, IObjectContext::SetComplete, SetComplete, SetComplete method [COM+], SetComplete method [COM+],IObjectContext interface, _cos_IObjectContext_SetComplete, comsvcs/IObjectContext::SetComplete, cos.iobjectcontext_setcomplete
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
-	IObjectContext.SetComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IObjectContext::SetComplete


## -description


Declares that the transaction in which the object is executing can be committed and that the object should be deactivated when it returns from the currently executing method call.


## -parameters






## -returns



This method can return the following values.

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
An unexpected error occurred. This can happen if one object passes its <a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a> pointer to another object and the other object calls <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a> using this pointer. An <b>IObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>
 




## -remarks



The object is deactivated automatically on return from the method in which it called <b>SetComplete</b>. If the object is the root of an automatic transaction, COM+ attempts to commit the transaction. However, if any object that was participating in the transaction has called <a href="https://msdn.microsoft.com/c254305f-1fc5-417e-b93b-d5e2b36e9e39">SetAbort</a>, or has called <a href="https://msdn.microsoft.com/e83d1223-9b8e-4a92-b98d-9d2b6ed34721">DisableCommit</a> and has not subsequently called <a href="https://msdn.microsoft.com/6571aadc-bf5a-48c3-817a-66ce444ef96a">EnableCommit</a> or <b>SetComplete</b>, the transaction is aborted.

If an object does not need to maintain its state after it returns from a method call, it should call <b>SetComplete</b> so that it can be automatically deactivated as soon as it returns and its resources can be reclaimed.




## -see-also




<a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a>
 

 

