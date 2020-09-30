---
UID: NN:azroles.IAzScope
title: IAzScope (azroles.h)
description: Defines a logical container of resources to which the application manages access.
helpviewer_keywords: ["IAzScope","IAzScope interface [Security]","IAzScope interface [Security]","described","azroles/IAzScope","security.iazscope"]
old-location: security\iazscope.htm
tech.root: security
ms.assetid: f7abe7cb-8827-46f6-85fe-99282582a3d4
ms.date: 12/05/2018
ms.keywords: IAzScope, IAzScope interface [Security], IAzScope interface [Security],described, azroles/IAzScope, security.iazscope
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzScope
 - azroles/IAzScope
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzScope
---

# IAzScope interface


## -description

The <b>IAzScope</b> interface defines a logical container of resources to which the application manages access. The scope name will be used in calls to the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method to determine whether a user has the requested access to resources logically contained within the scope.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzScope</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzScope</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzScope</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpolicyadministrator">AddPolicyAdministrator</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpolicyadministratorname">AddPolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpolicyreader">AddPolicyReader</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpolicyreadername">AddPolicyReaderName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpropertyitem">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified principal to the specified list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-createapplicationgroup">CreateApplicationGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-createrole">CreateRole</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-createtask">CreateTask</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-deleteapplicationgroup">DeleteApplicationGroup</a>
</td>
<td align="left" width="63%">
Removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-deletepolicyadministrator">DeletePolicyAdministrator</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-deletepolicyadministratorname">DeletePolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-deletepolicyreader">DeletePolicyReader</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-deletepolicyreadername">DeletePolicyReaderName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-deletepropertyitem">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified principal from the specified  list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-deleterole">DeleteRole</a>
</td>
<td align="left" width="63%">
Removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-deletetask">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzScope</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-openapplicationgroup">OpenApplicationGroup</a>
</td>
<td align="left" width="63%">
Opens an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-openrole">OpenRole</a>
</td>
<td align="left" width="63%">
Opens an <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-opentask">OpenTask</a>
</td>
<td align="left" width="63%">
Opens an <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>AzScope</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-submit">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>IAzScope</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzScope</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_applicationdata">ApplicationData</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves an opaque field that can be used by the application to store information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_applicationgroups">ApplicationGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroups">IAzApplicationGroups</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_bizruleswritable">BizrulesWritable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether a non-delegated scope is writable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_canbedelegated">CanBeDelegated</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the scope can be delegated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment that describes the scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_name">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyadministrators">PolicyAdministrators</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the text form of SIDs of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyadministratorsname">PolicyAdministratorsName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the account names of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyreaders">PolicyReaders</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the text form of SIDs of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyreadersname">PolicyReadersName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the account names of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_roles">Roles</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazroles">IAzRoles</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_tasks">Tasks</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iaztasks">IAzTasks</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_writable">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the scope can be modified by the  user context that initialized it.

</td>
</tr>
</table>