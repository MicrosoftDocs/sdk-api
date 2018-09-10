---
UID: NN:azroles.IAzRole
title: IAzRole
author: windows-sdk-content
description: Defines the set of operations that can be performed by a set of users within a scope.
old-location: security\iazrole.htm
tech.root: SecAuthZ
ms.assetid: 2934d783-b379-486c-80e7-e7650b89dc1a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAzRole, IAzRole interface [Security], IAzRole interface [Security],described, azroles/IAzRole, security.iazrole
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
 - IAzRole
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzRole interface


## -description


The <b>IAzRole</b> interface defines the set of operations that can be performed by a set of users within a scope.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRole</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAzRole</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzRole</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/118387f8-a422-4a8d-9d12-a5b5ee1e7b06">AddAppMember</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to the list of application groups that belong to this role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2be62cb-7256-4031-8af9-24f3043a8430">AddMember</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of Windows  accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc2ca62e-40b1-4b09-a129-50d6162c6807">AddMemberName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of  accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c6d26ff-3287-4a1d-91cb-759f79ec92e5">AddOperation</a>
</td>
<td align="left" width="63%">
Adds the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d9cb227-a3e8-4cd3-806a-5b7a38661b71">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified entity to the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51ba30c3-8067-4aca-b8aa-8e64d4427b98">AddTask</a>
</td>
<td align="left" width="63%">
Adds the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2856d75-cf16-4eec-a0e1-2e9e9fff601e">DeleteAppMember</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object from the list of application groups that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/676f0469-f57f-4f3f-8295-b9c99eb13de8">DeleteMember</a>
</td>
<td align="left" width="63%">
Removes  the specified SID in text form from the list of Windows  accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ca3e242-deab-46e7-b3f5-d6a75e5a2c08">DeleteMemberName</a>
</td>
<td align="left" width="63%">
Removes  the specified account name from the list of accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3486a12-7059-47b8-9f06-a025d5756b70">DeleteOperation</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name from the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79315dbc-70b4-4667-8187-9b26b971baee">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified entity from the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62623d45-33a6-4e3f-b0a8-d3e3e7c9e33e">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name from the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f65058ce-962d-4cad-9f55-c8b983ffaa05">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzRole</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f1c4abe-69cc-4672-8a74-eaaf55fc6e88">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>IAzRole</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">Submit</a>
</td>
<td align="left" width="63%">
Persists changes made to the <b>IAzRole</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRole</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6cb85528-35b4-4fed-98bb-6209dd0af0fd">ApplicationData</a>


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

<a href="https://msdn.microsoft.com/c41933d4-d3fe-485c-9249-e82d51c0bfc9">AppMembers</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the application groups that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2909c2ea-8308-49c3-9456-d035c1c242f0">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a comment that describes the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/03391842-fc8a-4dc2-878e-4fe1c41cc4dd">Members</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the text form of the SIDs of Windows  accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/defaefa8-2d76-49c6-bd1c-8b386f9dc5f1">MembersName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the account names of accounts that belong to the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fecd1cb8-55b8-4c7c-ba49-a633f9c8710c">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/44d90f1e-6112-4f02-b840-2ba7af8d9f33">Operations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the operations associated with the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/60342e8f-1947-4949-b25e-01db473712ac">Tasks</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the tasks associated with the role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/053b0ec4-143b-449d-bbbd-8ec8f00b0f2e">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the role can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

