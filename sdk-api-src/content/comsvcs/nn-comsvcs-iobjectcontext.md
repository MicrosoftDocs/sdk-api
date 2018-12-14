---
UID: NN:comsvcs.IObjectContext
title: IObjectContext
author: windows-sdk-content
description: Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.
old-location: cos\iobjectcontext.htm
tech.root: cossdk
ms.assetid: 9395bc9a-dfe5-428a-839f-1c4ad090f636
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IObjectContext, IObjectContext interface [COM+], IObjectContext interface [COM+],described, _cos_IObjectContext, comsvcs/IObjectContext, cos.iobjectcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IObjectContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectContext interface


## -description


Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e870191-5a34-490e-9f3a-cb646fe3f470">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an object using current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e83d1223-9b8e-4a92-b98d-9d2b6ed34721">DisableCommit</a>
</td>
<td align="left" width="63%">
Declares that the object's transactional updates are in an inconsistent state and cannot be committed in their present state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6571aadc-bf5a-48c3-817a-66ce444ef96a">EnableCommit</a>
</td>
<td align="left" width="63%">
Declares that the object's work is not necessarily finished but that its transactional updates are in a consistent state and could be committed in their present form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e545cc5-ad4e-43b9-a834-c9d470df24dd">IsCallerInRole</a>
</td>
<td align="left" width="63%">
Indicates whether the object's direct caller is in a specified role (either directly or as part of a group).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a5582ef-0142-45df-bdad-2e3d58ca6e87">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the object is executing within a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eba720e5-5c25-4723-b9e5-3bbdb69ada30">IsSecurityEnabled</a>
</td>
<td align="left" width="63%">
Indicates whether security is enabled for the current object. COM+ security is enabled unless the object is running in the client's process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c254305f-1fc5-417e-b93b-d5e2b36e9e39">SetAbort</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing must be aborted and that the object should be deactivated when it returns from the currently executing method call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing can be committed and that the object should be deactivated when it returns from the currently executing method call.

</td>
</tr>
</table> 


## -remarks



As with any COM object, you must release an <b>IObjectContext</b> object when you are finished using it, unless it is a local variable.




## -see-also




<a href="https://msdn.microsoft.com/97a0c6c3-a011-44dc-b428-aabdad7d4364">CoGetObjectContext</a>



<a href="https://msdn.microsoft.com/e93406df-e61c-4ee5-9cd4-828aab2c05b6">GetObjectContext</a>
 

 

