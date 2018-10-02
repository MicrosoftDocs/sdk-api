---
UID: NN:azroles.IAzApplication
title: IAzApplication
author: windows-sdk-content
description: Defines an installed instance of an application. An IAzApplication object is created when an application is installed.
old-location: security\iazapplication.htm
tech.root: SecAuthZ
ms.assetid: ea4a8a84-5003-44da-b75e-34da6bd898dd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAzApplication, IAzApplication interface [Security], IAzApplication interface [Security],described, azroles/IAzApplication, security.iazapplication
ms.prod: windows
ms.technology: windows-sdk
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
 - IAzApplication
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication interface


## -description


The <b>IAzApplication</b> interface defines an installed instance of an application. An <b>IAzApplication</b> object is created when an application is installed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplication</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAzApplication</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/89c0e1b9-cf51-4f4f-b530-7982645a9d14">AddDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f30392f6-7100-43dd-ab20-419cd02d9ea5">AddDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/944f93c1-5155-4c87-a241-9fdef84b68fc">AddPolicyAdministrator</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc5f74c6-e1b6-4924-b5c1-2d3600ce37ef">AddPolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb44461c-e494-4393-bdcd-0e759f6fbae1">AddPolicyReader</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc81527a-7a38-4c5c-857e-bedcda5a5ac3">AddPolicyReaderName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377336(v=VS.85).aspx">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified principal to the specified list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377341(v=VS.85).aspx">CreateApplicationGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377342(v=VS.85).aspx">CreateOperation</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377343(v=VS.85).aspx">CreateRole</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa377917(v=VS.85).aspx">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377344(v=VS.85).aspx">CreateScope</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa378237(v=VS.85).aspx">IAzScope</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377345(v=VS.85).aspx">CreateTask</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377348(v=VS.85).aspx">DeleteApplicationGroup</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377349(v=VS.85).aspx">DeleteDelegatedPolicyUser</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377350(v=VS.85).aspx">DeleteDelegatedPolicyUserName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as delegated policy users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377351(v=VS.85).aspx">DeleteOperation</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377352(v=VS.85).aspx">DeletePolicyAdministrator</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377353(v=VS.85).aspx">DeletePolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377354(v=VS.85).aspx">DeletePolicyReader</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377355(v=VS.85).aspx">DeletePolicyReaderName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377356(v=VS.85).aspx">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified principal from the specified  list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377357(v=VS.85).aspx">DeleteRole</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377917(v=VS.85).aspx">IAzRole</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377358(v=VS.85).aspx">DeleteScope</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa378237(v=VS.85).aspx">IAzScope</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377359(v=VS.85).aspx">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object with the specified name from the <b>IAzApplication</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377362(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzApplication</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377363(v=VS.85).aspx">InitializeClientContextFromName</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Aa377837(v=VS.85).aspx">IAzClientContext</a> object pointer from the client identity as a (domain name, client name) pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377364(v=VS.85).aspx">InitializeClientContextFromStringSid</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Aa377837(v=VS.85).aspx">IAzClientContext</a> object pointer from the specified SID in text form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377365(v=VS.85).aspx">InitializeClientContextFromToken</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Aa377837(v=VS.85).aspx">IAzClientContext</a> object pointer from the specified client token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377367(v=VS.85).aspx">OpenApplicationGroup</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377368(v=VS.85).aspx">OpenOperation</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377369(v=VS.85).aspx">OpenRole</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa377917(v=VS.85).aspx">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377370(v=VS.85).aspx">OpenScope</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa378237(v=VS.85).aspx">IAzScope</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377371(v=VS.85).aspx">OpenTask</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377558(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzApplication</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377565(v=VS.85).aspx">Submit</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377337(v=VS.85).aspx">ApplicationData</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377338(v=VS.85).aspx">ApplicationGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377293(v=VS.85).aspx">IAzApplicationGroups</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377339(v=VS.85).aspx">ApplyStoreSacl</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377340(v=VS.85).aspx">AuthzInterfaceClsid</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377346(v=VS.85).aspx">DelegatedPolicyUsers</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377347(v=VS.85).aspx">DelegatedPolicyUsersName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377360(v=VS.85).aspx">Description</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377361(v=VS.85).aspx">GenerateAudits</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377366(v=VS.85).aspx">Name</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377372(v=VS.85).aspx">Operations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377902(v=VS.85).aspx">IAzOperations</a> object that is used to enumerate operations from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377373(v=VS.85).aspx">PolicyAdministrators</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377374(v=VS.85).aspx">PolicyAdministratorsName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377375(v=VS.85).aspx">PolicyReaders</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377376(v=VS.85).aspx">PolicyReadersName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377377(v=VS.85).aspx">Roles</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377936(v=VS.85).aspx">IAzRoles</a> object that is used to enumerate roles from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377551(v=VS.85).aspx">Scopes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa378272(v=VS.85).aspx">IAzScopes</a> object that is used to enumerate scopes from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377572(v=VS.85).aspx">Tasks</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa378370(v=VS.85).aspx">IAzTasks</a> object that is used to enumerate tasks from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377574(v=VS.85).aspx">Version</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa377579(v=VS.85).aspx">Writable</a>


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




<a href="https://msdn.microsoft.com/en-us/library/Aa375347(v=VS.85).aspx">Allowing Anonymous Access</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

