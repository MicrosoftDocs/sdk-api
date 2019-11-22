---
UID: NN:comsvcs.ObjectContext
title: ObjectContext (comsvcs.h)

description: Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.
old-location: cos\objectcontext.htm
tech.root: cossdk
ms.assetid: 09a17e57-7224-43bc-93c7-16ab95ca2517

ms.date: 12/05/2018
ms.keywords: ObjectContext, ObjectContext interface [COM+], ObjectContext interface [COM+],described, _cos_ObjectContext, comsvcs/ObjectContext, cos.objectcontext
ms.topic: interface
f1_keywords: 
 - "comsvcs/ObjectContext"
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
 - ObjectContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ObjectContext interface


## -description


Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.

<b>ObjectContext</b> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> provide the same functionality, but unlike <b>IObjectContext</b>, <b>ObjectContext</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ObjectContext</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ObjectContext</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an object using current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-disablecommit">DisableCommit</a>
</td>
<td align="left" width="63%">
Declares that the object's transactional updates are inconsistent and cannot be committed in their present state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-enablecommit">EnableCommit</a>
</td>
<td align="left" width="63%">
Declares that the current object's work is not necessarily finished but that its transactional updates are consistent and could be committed in their present form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the named context object properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-get_contextinfo">get_ContextInfo</a>
</td>
<td align="left" width="63%">
Retrieves the context information object of the current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of named context object properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a named property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-get_security">get_Security</a>
</td>
<td align="left" width="63%">
Retrieves the security object of the current object's context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-iscallerinrole">IsCallerInRole</a>
</td>
<td align="left" width="63%">
Indicates whether the object's direct caller is in a specified role (either directly or as part of a group).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-isintransaction">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the current object is executing in a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-issecurityenabled">IsSecurityEnabled</a>
</td>
<td align="left" width="63%">
Indicates whether security is enabled for the current object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-setabort">SetAbort</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing must be aborted and that the object should be deactivated on return.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-setcomplete">SetComplete</a>
</td>
<td align="left" width="63%">
Declares that the transaction in which the object is executing can be committed and that the object should be deactivated on return.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
 

 

