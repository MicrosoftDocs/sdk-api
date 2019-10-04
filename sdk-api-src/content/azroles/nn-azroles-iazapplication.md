---
UID: NN:azroles.IAzApplication
title: IAzApplication (azroles.h)
author: windows-sdk-content
description: Defines an installed instance of an application. An IAzApplication object is created when an application is installed.
old-location: security\iazapplication.htm
tech.root: SecAuthZ
ms.assetid: ea4a8a84-5003-44da-b75e-34da6bd898dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzApplication, IAzApplication interface [Security], IAzApplication interface [Security],described, azroles/IAzApplication, security.iazapplication
ms.topic: interface
f1_keywords: 
 - "azroles/IAzApplication"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplication interface


## -description


The <b>IAzApplication</b> interface defines an installed instance of an application. An <b>IAzApplication</b> object is created when an application is installed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplication</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-adddelegatedpolicyuser">AddDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-adddelegatedpolicyusername">AddDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-addpolicyadministrator">AddPolicyAdministrator</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-addpolicyadministratorname">AddPolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-addpolicyreader">AddPolicyReader</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-addpolicyreadername">AddPolicyReaderName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-addpropertyitem">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified principal to the specified list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-createapplicationgroup">CreateApplicationGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-createoperation">CreateOperation</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-createrole">CreateRole</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-createscope">CreateScope</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-createtask">CreateTask</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deleteapplicationgroup">DeleteApplicationGroup</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletedelegatedpolicyuser">DeleteDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletedelegatedpolicyusername">DeleteDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deleteoperation">DeleteOperation</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepolicyadministrator">DeletePolicyAdministrator</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepolicyadministratorname">DeletePolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepolicyreader">DeletePolicyReader</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepolicyreadername">DeletePolicyReaderName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepropertyitem">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified principal from the specified  list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deleterole">DeleteRole</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletescope">DeleteScope</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-deletetask">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzApplication</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-initializeclientcontextfromname">InitializeClientContextFromName</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object pointer from the client identity as a (domain name, client name) pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid">InitializeClientContextFromStringSid</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object pointer from the specified SID in text form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken">InitializeClientContextFromToken</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object pointer from the specified client token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-openapplicationgroup">OpenApplicationGroup</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-openoperation">OpenOperation</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-openrole">OpenRole</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-openscope">OpenScope</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-opentask">OpenTask</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzApplication</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>IAzApplication</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplication</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_applicationdata">ApplicationData</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_applicationgroups">ApplicationGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroups">IAzApplicationGroups</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_applystoresacl">ApplyStoreSacl</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether policy audits should be generated when the authorization store is modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_authzinterfaceclsid">AuthzInterfaceClsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the class identifier of the interface that the user interface uses to perform application-specific operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_delegatedpolicyusers">DelegatedPolicyUsers</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the SIDs (in text form) of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_delegatedpolicyusersname">DelegatedPolicyUsersName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the account names of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment that describes the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_generateaudits">GenerateAudits</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that indicates whether run-time audits should be generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_name">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_operations">Operations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperations">IAzOperations</a> object that is used to enumerate operations from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyadministrators">PolicyAdministrators</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the SIDs (in text form) of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyadministratorsname">PolicyAdministratorsName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyreaders">PolicyReaders</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the SIDs (in text form) of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyreadersname">PolicyReadersName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_roles">Roles</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroles">IAzRoles</a> object that is used to enumerate roles from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_scopes">Scopes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazscopes">IAzScopes</a> object that is used to enumerate scopes from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_tasks">Tasks</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztasks">IAzTasks</a> object that is used to enumerate tasks from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_version">Version</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the version of the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-get_writable">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the application can be modified by the  user context that initialized it.

</td>
</tr>
</table> 


## -remarks



The <b>IAzApplication</b> object is a container in which all authorization policies that apply to an instance of an application reside.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/allowing-anonymous-access">Allowing Anonymous Access</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

