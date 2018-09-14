---
UID: NN:comsvcs.ObjectContext
title: ObjectContext
author: windows-sdk-content
description: Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.
old-location: cos\objectcontext.htm
tech.root: cossdk
ms.assetid: 09a17e57-7224-43bc-93c7-16ab95ca2517
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ObjectContext, ObjectContext interface [COM+], ObjectContext interface [COM+],described, _cos_ObjectContext, comsvcs/ObjectContext, cos.objectcontext
ms.prod: windows
ms.technology: windows-sdk
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
 - ObjectContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ObjectContext interface


## -description


Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.

<b>ObjectContext</b> and <a href="https://msdn.microsoft.com/en-us/library/ms684253(v=VS.85).aspx">IObjectContext</a> provide the same functionality, but unlike <b>IObjectContext</b>, <b>ObjectContext</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ObjectContext</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ObjectContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ObjectContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9719f672-d706-44e3-b976-28d0d0feacd1">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an object using current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf0e59d9-2760-445e-aa7d-8c2b78457181">DisableCommit</a>
</td>
<td align="left" width="63%">
Declares that the object's transactional updates are inconsistent and cannot be committed in their present state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686436(v=VS.85).aspx">EnableCommit</a>
</td>
<td align="left" width="63%">
Declares that the current object's work is not necessarily finished but that its transactional updates are consistent and could be committed in their present form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681293(v=VS.85).aspx">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the named context object properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679204(v=VS.85).aspx">get_ContextInfo</a>
</td>
<td align="left" width="63%">
Retrieves the context information object of the current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678900(v=VS.85).aspx">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of named context object properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688477(v=VS.85).aspx">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a named property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685083(v=VS.85).aspx">get_Security</a>
</td>
<td align="left" width="63%">
Retrieves the security object of the current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687109(v=VS.85).aspx">IsCallerInRole</a>
</td>
<td align="left" width="63%">
Indicates whether the object's direct caller is in a specified role (either directly or as part of a group).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683556(v=VS.85).aspx">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the current object is executing in a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686450(v=VS.85).aspx">IsSecurityEnabled</a>
</td>
<td align="left" width="63%">
Indicates whether security is enabled for the current object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682326(v=VS.85).aspx">SetAbort</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing must be aborted and that the object should be deactivated on return.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680210(v=VS.85).aspx">SetComplete</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing can be committed and that the object should be deactivated on return.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684253(v=VS.85).aspx">IObjectContext</a>
 

 

