---
UID: NN:comsvcs.IObjectContext
title: IObjectContext (comsvcs.h)
description: Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.helpviewer_keywords: ["IObjectContext","IObjectContext interface [COM+]","IObjectContext interface [COM+]","described","_cos_IObjectContext","comsvcs/IObjectContext","cos.iobjectcontext"]
old-location: cos\iobjectcontext.htm
tech.root: cossdk
ms.assetid: 9395bc9a-dfe5-428a-839f-1c4ad090f636
ms.date: 12/05/2018
ms.keywords: IObjectContext, IObjectContext interface [COM+], IObjectContext interface [COM+],described, _cos_IObjectContext, comsvcs/IObjectContext, cos.iobjectcontext
f1_keywords:
- comsvcs/IObjectContext
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectContext interface


## -description


Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectContext</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an object using current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-disablecommit">DisableCommit</a>
</td>
<td align="left" width="63%">
Declares that the object's transactional updates are in an inconsistent state and cannot be committed in their present state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">EnableCommit</a>
</td>
<td align="left" width="63%">
Declares that the object's work is not necessarily finished but that its transactional updates are in a consistent state and could be committed in their present form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-iscallerinrole">IsCallerInRole</a>
</td>
<td align="left" width="63%">
Indicates whether the object's direct caller is in a specified role (either directly or as part of a group).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-isintransaction">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the object is executing within a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-issecurityenabled">IsSecurityEnabled</a>
</td>
<td align="left" width="63%">
Indicates whether security is enabled for the current object. COM+ security is enabled unless the object is running in the client's process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing must be aborted and that the object should be deactivated when it returns from the currently executing method call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing can be committed and that the object should be deactivated when it returns from the currently executing method call.

</td>
</tr>
</table> 


## -remarks



As with any COM object, you must release an <b>IObjectContext</b> object when you are finished using it, unless it is a local variable.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-getobjectcontext">GetObjectContext</a>
 

 

