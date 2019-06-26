---
UID: NN:azroles.IAzAuthorizationStore
title: IAzAuthorizationStore (azroles.h)
author: windows-sdk-content
description: Defines the container that is the root of the authorization policy store.
old-location: security\azauthorizationstore.htm
tech.root: SecAuthZ
ms.assetid: f848cca6-3838-46bc-b1f4-d6eab5096046
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzAuthorizationStore, IAzAuthorizationStore interface [Security], IAzAuthorizationStore interface [Security],described, azroles/IAzAuthorizationStore, security.azauthorizationstore
ms.topic: interface
f1_keywords: 
 - "azroles/IAzAuthorizationStore"
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
 - IAzAuthorizationStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzAuthorizationStore interface


## -description


The <b>AzAuthorizationStore</b> object defines the container that is the root of the authorization policy store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzAuthorizationStore</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAzAuthorizationStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzAuthorizationStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser">AddDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyusername">AddDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyadministrator">AddPolicyAdministrator</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyadministratorname">AddPolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyreader">AddPolicyReader</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as policy readers. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyreadername">AddPolicyReaderName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpropertyitem">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified principal to the specified  list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-closeapplication">CloseApplication</a>
</td>
<td align="left" width="63%">
Unloads a specified <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-createapplication">CreateApplication</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-createapplicationgroup">CreateApplicationGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the policy store currently in use by the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deleteapplication">DeleteApplication</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object with the specified name from the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deleteapplicationgroup">DeleteApplicationGroup</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name from the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deletedelegatedpolicyuser">DeleteDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deletedelegatedpolicyusername">DeleteDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deletepolicyadministrator">DeletePolicyAdministrator</a>
</td>
<td align="left" width="63%">
Deletes the specified SID in text form from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deletepolicyadministratorname">DeletePolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deletepolicyreader">DeletePolicyReader</a>
</td>
<td align="left" width="63%">
Deletes the specified SID in text form from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deletepolicyreadername">DeletePolicyReaderName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-deletepropertyitem">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified principal from the specified list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>AzAuthorizationStore</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the authorization manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-openapplication">OpenApplication</a>
</td>
<td align="left" width="63%">
Opens the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-openapplicationgroup">OpenApplicationGroup</a>
</td>
<td align="left" width="63%">
Opens the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>AzAuthorizationStore</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-updatecache">UpdateCache</a>
</td>
<td align="left" width="63%">
Updates the cache of objects and object attributes to match the underlying policy store.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzAuthorizationStore</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_applicationdata">ApplicationData</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_applicationgroups">ApplicationGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroups</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_applications">Applications</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplications">IAzApplications</a> object that is used to enumerate applications from the policy store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_applystoresacl">ApplyStoreSacl</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_delegatedpolicyusers">DelegatedPolicyUsers</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the SIDs of principals that act as delegated policy users in text form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_delegatedpolicyusersname">DelegatedPolicyUsersName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment describing the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_domaintimeout">DomainTimeout</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the time in milliseconds after which a domain is determined to be unreachable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_generateaudits">GenerateAudits</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_maxscriptengines">MaxScriptEngines</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the maximum number of Business Rule (BizRule) script engines that will be cached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyadministrators">PolicyAdministrators</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the SIDs of principals that act as policy administrators in text form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyadministratorsname">PolicyAdministratorsName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyreaders">PolicyReaders</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the SIDs of principals that act as policy readers in text form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyreadersname">PolicyReadersName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_scriptenginetimeout">ScriptEngineTimeout</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the time in milliseconds that the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">IAzClientContext::AccessCheck</a> method will wait for a BizRule to complete execution before canceling  it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_targetmachine">TargetMachine</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the computer on which account resolution should occur.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_writable">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the object can be modified by the user context that called the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-initialize">Initialize</a> method.

</td>
</tr>
</table> 


## -remarks



The <b>AzAuthorizationStore</b> object is named according to the URL passed to the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-initialize">Initialize</a> method. The object has no name within  the policy store.

The application must ensure that the user context from which the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-initialize">Initialize</a> method is called is used for all future access to the <b>AzAuthorizationStore</b> object, except for the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken">IAzApplication::InitializeClientContextFromToken</a> method.

<div class="alert"><b>Note</b>  If an XML store is used over a network, the traffic is not automatically encrypted. IPsec can be used to encrypt the authorization information in transit.</div>
<div> </div>


