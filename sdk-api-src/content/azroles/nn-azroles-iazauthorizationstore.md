---
UID: NN:azroles.IAzAuthorizationStore
title: IAzAuthorizationStore
author: windows-sdk-content
description: Defines the container that is the root of the authorization policy store.
old-location: security\azauthorizationstore.htm
tech.root: SecAuthZ
ms.assetid: f848cca6-3838-46bc-b1f4-d6eab5096046
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAzAuthorizationStore, IAzAuthorizationStore interface [Security], IAzAuthorizationStore interface [Security],described, azroles/IAzAuthorizationStore, security.azauthorizationstore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IAzAuthorizationStore interface


## -description


The <b>AzAuthorizationStore</b> object defines the container that is the root of the authorization policy store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzAuthorizationStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAzAuthorizationStore</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0c6714e9-489e-4266-a8b5-35c66b0a14f4">AddDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9eeb4670-a3be-46dd-83b4-4ab12a311fe3">AddDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d73bc05-1366-4b47-9eaf-4a247ebf8d93">AddPolicyAdministrator</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376331(v=VS.85).aspx">AddPolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376332(v=VS.85).aspx">AddPolicyReader</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as policy readers. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376334(v=VS.85).aspx">AddPolicyReaderName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376335(v=VS.85).aspx">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified principal to the specified  list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376340(v=VS.85).aspx">CloseApplication</a>
</td>
<td align="left" width="63%">
Unloads a specified <a href="https://msdn.microsoft.com/en-us/library/Aa446684(v=VS.85).aspx">IAzApplication</a> object from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376341(v=VS.85).aspx">CreateApplication</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa446684(v=VS.85).aspx">IAzApplication</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376342(v=VS.85).aspx">CreateApplicationGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376345(v=VS.85).aspx">Delete</a>
</td>
<td align="left" width="63%">
Deletes the policy store currently in use by the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376346(v=VS.85).aspx">DeleteApplication</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa446684(v=VS.85).aspx">IAzApplication</a> object with the specified name from the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376347(v=VS.85).aspx">DeleteApplicationGroup</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name from the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376348(v=VS.85).aspx">DeleteDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376349(v=VS.85).aspx">DeleteDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376350(v=VS.85).aspx">DeletePolicyAdministrator</a>
</td>
<td align="left" width="63%">
Deletes the specified SID in text form from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376351(v=VS.85).aspx">DeletePolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376352(v=VS.85).aspx">DeletePolicyReader</a>
</td>
<td align="left" width="63%">
Deletes the specified SID in text form from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376353(v=VS.85).aspx">DeletePolicyReaderName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376354(v=VS.85).aspx">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified principal from the specified list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376358(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>AzAuthorizationStore</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376359(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the authorization manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376361(v=VS.85).aspx">OpenApplication</a>
</td>
<td align="left" width="63%">
Opens the <a href="https://msdn.microsoft.com/en-us/library/Aa446684(v=VS.85).aspx">IAzApplication</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376362(v=VS.85).aspx">OpenApplicationGroup</a>
</td>
<td align="left" width="63%">
Opens the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376368(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>AzAuthorizationStore</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376369(v=VS.85).aspx">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376371(v=VS.85).aspx">UpdateCache</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa376336(v=VS.85).aspx">ApplicationData</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376337(v=VS.85).aspx">ApplicationGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroups</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376338(v=VS.85).aspx">Applications</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377325(v=VS.85).aspx">IAzApplications</a> object that is used to enumerate applications from the policy store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376339(v=VS.85).aspx">ApplyStoreSacl</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376343(v=VS.85).aspx">DelegatedPolicyUsers</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376344(v=VS.85).aspx">DelegatedPolicyUsersName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376355(v=VS.85).aspx">Description</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376356(v=VS.85).aspx">DomainTimeout</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376357(v=VS.85).aspx">GenerateAudits</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376360(v=VS.85).aspx">MaxScriptEngines</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376363(v=VS.85).aspx">PolicyAdministrators</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376364(v=VS.85).aspx">PolicyAdministratorsName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376365(v=VS.85).aspx">PolicyReaders</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376366(v=VS.85).aspx">PolicyReadersName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376367(v=VS.85).aspx">ScriptEngineTimeout</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the time in milliseconds that the <a href="https://msdn.microsoft.com/en-us/library/Aa377880(v=VS.85).aspx">IAzClientContext::AccessCheck</a> method will wait for a BizRule to complete execution before canceling  it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376370(v=VS.85).aspx">TargetMachine</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa376372(v=VS.85).aspx">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the object can be modified by the user context that called the <a href="https://msdn.microsoft.com/en-us/library/Aa376359(v=VS.85).aspx">Initialize</a> method.

</td>
</tr>
</table> 


## -remarks



The <b>AzAuthorizationStore</b> object is named according to the URL passed to the <a href="https://msdn.microsoft.com/en-us/library/Aa376359(v=VS.85).aspx">Initialize</a> method. The object has no name within  the policy store.

The application must ensure that the user context from which the <a href="https://msdn.microsoft.com/en-us/library/Aa376359(v=VS.85).aspx">Initialize</a> method is called is used for all future access to the <b>AzAuthorizationStore</b> object, except for the <a href="https://msdn.microsoft.com/en-us/library/Aa377365(v=VS.85).aspx">IAzApplication::InitializeClientContextFromToken</a> method.

<div class="alert"><b>Note</b>  If an XML store is used over a network, the traffic is not automatically encrypted. IPsec can be used to encrypt the authorization information in transit.</div>
<div> </div>


