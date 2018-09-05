---
UID: NN:azroles.IAzAuthorizationStore
title: IAzAuthorizationStore
author: windows-sdk-content
description: Defines the container that is the root of the authorization policy store.
old-location: security\azauthorizationstore.htm
old-project: SecAuthZ
ms.assetid: f848cca6-3838-46bc-b1f4-d6eab5096046
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAzAuthorizationStore, IAzAuthorizationStore interface [Security], IAzAuthorizationStore interface [Security],described, azroles/IAzAuthorizationStore, security.azauthorizationstore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
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
<a href="https://msdn.microsoft.com/b77348c7-4389-47ba-9f4f-e5643cf992aa">AddPolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52872839-1066-4a43-8549-b7f37a0ebe40">AddPolicyReader</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as policy readers. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b111542-61d6-4e5d-abf8-0af61161c885">AddPolicyReaderName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88ac498c-2871-4260-8011-0aea9e6c346d">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified principal to the specified  list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ba5fc77-676a-4fbe-8de8-2af5bf5f82f6">CloseApplication</a>
</td>
<td align="left" width="63%">
Unloads a specified <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca6feb69-15cd-454a-a2b8-c75c4c6b38cd">CreateApplication</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9a78aaa-189b-4878-a5ba-fb6fb8927c5e">CreateApplicationGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8493af39-c5db-4aeb-839f-bc07e2616443">Delete</a>
</td>
<td align="left" width="63%">
Deletes the policy store currently in use by the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/512907fc-8657-4f2a-8b4a-af3027c6bbcd">DeleteApplication</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object with the specified name from the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2b89378-9b4e-411f-b856-51053b649996">DeleteApplicationGroup</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name from the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb00abca-7116-4a71-aed0-87ed9caff0fb">DeleteDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2e7523a-41d3-4fb5-b455-588e0618f51f">DeleteDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c27ca754-7808-4c96-8966-0be3960f2926">DeletePolicyAdministrator</a>
</td>
<td align="left" width="63%">
Deletes the specified SID in text form from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28be14c8-9e39-4410-a08c-b52bb63d0ce4">DeletePolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948732bb-4d29-402b-bb12-02d2b73bc443">DeletePolicyReader</a>
</td>
<td align="left" width="63%">
Deletes the specified SID in text form from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3375c24-82c3-43fd-a063-8c8079324641">DeletePolicyReaderName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c204a3c-2c5b-44d3-bbab-2765e66da925">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified principal from the specified list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93bd6813-cc46-4f48-b39b-1e67cda562ff">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>AzAuthorizationStore</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c461d50a-c785-4b32-b331-fe3a1693f4de">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the authorization manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63215a9a-b739-4ba9-a760-a9968be9e017">OpenApplication</a>
</td>
<td align="left" width="63%">
Opens the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30860261-c792-4610-b217-7c4d58554778">OpenApplicationGroup</a>
</td>
<td align="left" width="63%">
Opens the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c71a022f-8244-4263-8ff6-6c2d9562fcd1">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>AzAuthorizationStore</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>AzAuthorizationStore</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fd17040-f736-44a6-8a01-720f4c8fe9ac">UpdateCache</a>
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

<a href="https://msdn.microsoft.com/21a76185-6bcf-405a-a2c5-5509b51ed16e">ApplicationData</a>


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

<a href="https://msdn.microsoft.com/02bab92b-b234-4755-a4d3-f787fe46252d">ApplicationGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroups</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7475fe41-b2fc-4a2c-a0db-c8c00bcc3ba4">Applications</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/04cee21c-253a-463a-9231-592ddad88188">IAzApplications</a> object that is used to enumerate applications from the policy store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fdace7a9-4b6b-4698-812d-c53fc3b8f0d8">ApplyStoreSacl</a>


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

<a href="https://msdn.microsoft.com/cc1268d5-d386-4888-a987-e40896a096e4">DelegatedPolicyUsers</a>


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

<a href="https://msdn.microsoft.com/495cdba4-7127-48aa-9542-7ccbedbad589">DelegatedPolicyUsersName</a>


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

<a href="https://msdn.microsoft.com/79ef0e2f-3178-4310-832c-b0eea06cf1b0">Description</a>


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

<a href="https://msdn.microsoft.com/e512641d-a282-41f6-a7d8-5383ad43cd5b">DomainTimeout</a>


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

<a href="https://msdn.microsoft.com/e9362ae0-488d-4b6b-9a7b-c70fd85042ca">GenerateAudits</a>


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

<a href="https://msdn.microsoft.com/d18fe030-5177-4516-b4bf-6fea78abea52">MaxScriptEngines</a>


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

<a href="https://msdn.microsoft.com/388d4970-5de4-4216-8c26-b9b24cc82ca3">PolicyAdministrators</a>


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

<a href="https://msdn.microsoft.com/20f84f75-ad27-4329-90a8-46e7d817863f">PolicyAdministratorsName</a>


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

<a href="https://msdn.microsoft.com/22479ced-b393-40d3-bb16-f3c3e595dacf">PolicyReaders</a>


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

<a href="https://msdn.microsoft.com/d550448e-a1ea-45f3-9151-affd4b8c0b14">PolicyReadersName</a>


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

<a href="https://msdn.microsoft.com/7ac3db2d-11a6-4481-a86d-4b3a1063dee3">ScriptEngineTimeout</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the time in milliseconds that the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">IAzClientContext::AccessCheck</a> method will wait for a BizRule to complete execution before canceling  it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/60c3c23a-4721-4f0d-8380-e95b6170c804">TargetMachine</a>


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

<a href="https://msdn.microsoft.com/0c896364-739a-456a-97f7-0448711462b3">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the object can be modified by the user context that called the <a href="https://msdn.microsoft.com/c461d50a-c785-4b32-b331-fe3a1693f4de">Initialize</a> method.

</td>
</tr>
</table> 


## -remarks



The <b>AzAuthorizationStore</b> object is named according to the URL passed to the <a href="https://msdn.microsoft.com/c461d50a-c785-4b32-b331-fe3a1693f4de">Initialize</a> method. The object has no name within  the policy store.

The application must ensure that the user context from which the <a href="https://msdn.microsoft.com/c461d50a-c785-4b32-b331-fe3a1693f4de">Initialize</a> method is called is used for all future access to the <b>AzAuthorizationStore</b> object, except for the <a href="https://msdn.microsoft.com/0002804d-0e97-4648-8aa1-14eba09a90fa">IAzApplication::InitializeClientContextFromToken</a> method.

<div class="alert"><b>Note</b>  If an XML store is used over a network, the traffic is not automatically encrypted. IPsec can be used to encrypt the authorization information in transit.</div>
<div> </div>


