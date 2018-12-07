---
UID: NN:azroles.IAzScope
title: IAzScope
author: windows-sdk-content
description: Defines a logical container of resources to which the application manages access.
old-location: security\iazscope.htm
tech.root: secauthz
ms.assetid: f7abe7cb-8827-46f6-85fe-99282582a3d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAzScope, IAzScope interface [Security], IAzScope interface [Security],described, azroles/IAzScope, security.iazscope
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
 - IAzScope
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope interface


## -description


The <b>IAzScope</b> interface defines a logical container of resources to which the application manages access. The scope name will be used in calls to the <a href="https://msdn.microsoft.com/en-us/library/Aa377880(v=VS.85).aspx">AccessCheck</a> method to determine whether a user has the requested access to resources logically contained within the scope.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzScope</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAzScope</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa378287(v=VS.85).aspx">AddPolicyAdministrator</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378291(v=VS.85).aspx">AddPolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378293(v=VS.85).aspx">AddPolicyReader</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378294(v=VS.85).aspx">AddPolicyReaderName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378298(v=VS.85).aspx">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified principal to the specified list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378312(v=VS.85).aspx">CreateApplicationGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378315(v=VS.85).aspx">CreateRole</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa377917(v=VS.85).aspx">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378317(v=VS.85).aspx">CreateTask</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378320(v=VS.85).aspx">DeleteApplicationGroup</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378341(v=VS.85).aspx">DeletePolicyAdministrator</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378345(v=VS.85).aspx">DeletePolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378347(v=VS.85).aspx">DeletePolicyReader</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378348(v=VS.85).aspx">DeletePolicyReaderName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378349(v=VS.85).aspx">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified principal from the specified  list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378350(v=VS.85).aspx">DeleteRole</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377917(v=VS.85).aspx">IAzRole</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378351(v=VS.85).aspx">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378353(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzScope</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378355(v=VS.85).aspx">OpenApplicationGroup</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378356(v=VS.85).aspx">OpenRole</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa377917(v=VS.85).aspx">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378357(v=VS.85).aspx">OpenTask</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/en-us/library/Aa378367(v=VS.85).aspx">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378363(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>AzScope</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378364(v=VS.85).aspx">Submit</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa378301(v=VS.85).aspx">ApplicationData</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378304(v=VS.85).aspx">ApplicationGroups</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378306(v=VS.85).aspx">BizrulesWritable</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378309(v=VS.85).aspx">CanBeDelegated</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378352(v=VS.85).aspx">Description</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378354(v=VS.85).aspx">Name</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378358(v=VS.85).aspx">PolicyAdministrators</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378359(v=VS.85).aspx">PolicyAdministratorsName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378360(v=VS.85).aspx">PolicyReaders</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378361(v=VS.85).aspx">PolicyReadersName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa378362(v=VS.85).aspx">Roles</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377936(v=VS.85).aspx">IAzRoles</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378365(v=VS.85).aspx">Tasks</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa378370(v=VS.85).aspx">IAzTasks</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378366(v=VS.85).aspx">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the scope can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

