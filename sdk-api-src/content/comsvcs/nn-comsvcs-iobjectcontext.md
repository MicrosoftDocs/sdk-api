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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContext</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IObjectContext</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms679540(v=VS.85).aspx">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an object using current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687629(v=VS.85).aspx">DisableCommit</a>
</td>
<td align="left" width="63%">
Declares that the object's transactional updates are in an inconsistent state and cannot be committed in their present state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681803(v=VS.85).aspx">EnableCommit</a>
</td>
<td align="left" width="63%">
Declares that the object's work is not necessarily finished but that its transactional updates are in a consistent state and could be committed in their present form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684182(v=VS.85).aspx">IsCallerInRole</a>
</td>
<td align="left" width="63%">
Indicates whether the object's direct caller is in a specified role (either directly or as part of a group).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682206(v=VS.85).aspx">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the object is executing within a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687698(v=VS.85).aspx">IsSecurityEnabled</a>
</td>
<td align="left" width="63%">
Indicates whether security is enabled for the current object. COM+ security is enabled unless the object is running in the client's process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686120(v=VS.85).aspx">SetAbort</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing must be aborted and that the object should be deactivated when it returns from the currently executing method call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684201(v=VS.85).aspx">SetComplete</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing can be committed and that the object should be deactivated when it returns from the currently executing method call.

</td>
</tr>
</table> 


## -remarks



As with any COM object, you must release an <b>IObjectContext</b> object when you are finished using it, unless it is a local variable.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690084(v=VS.85).aspx">CoGetObjectContext</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687640(v=VS.85).aspx">GetObjectContext</a>
 

 

