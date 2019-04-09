---
UID: NN:azroles.IAzScope
title: IAzScope (azroles.h)
author: windows-sdk-content
description: Defines a logical container of resources to which the application manages access.
old-location: security\iazscope.htm
tech.root: SecAuthZ
ms.assetid: f7abe7cb-8827-46f6-85fe-99282582a3d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzScope, IAzScope interface [Security], IAzScope interface [Security],described, azroles/IAzScope, security.iazscope
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


The <b>IAzScope</b> interface defines a logical container of resources to which the application manages access. The scope name will be used in calls to the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method to determine whether a user has the requested access to resources logically contained within the scope.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzScope</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAzScope</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7aa77615-1f12-4641-877e-87b26343db4d">AddPolicyAdministrator</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a160e4cb-e779-413e-9d8a-5fb9684a48f2">AddPolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd4d3254-8bcf-46b5-8e7b-d3f076988a7c">AddPolicyReader</a>
</td>
<td align="left" width="63%">
Adds the specified SID in text form to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6beb02cb-7977-4f3f-b806-420c81f6f0b5">AddPolicyReaderName</a>
</td>
<td align="left" width="63%">
Adds the specified account name to the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5170079b-9ea6-417c-87f2-bb8835225911">AddPropertyItem</a>
</td>
<td align="left" width="63%">
Adds the specified principal to the specified list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bceb3a9-1144-48a1-a4d4-e612a3e77942">CreateApplicationGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5e527f9-0aab-40d9-83fe-f19f73673266">CreateRole</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2be1afd7-8d10-4783-a5ea-3e8c0b103ceb">CreateTask</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9571bff3-dfe5-48fa-be51-38d61da40414">DeleteApplicationGroup</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23077da5-5475-45c6-87c0-b38f6c05d386">DeletePolicyAdministrator</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6314e1d5-e5ea-42c4-9457-dad5d6f57897">DeletePolicyAdministratorName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy administrators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c328a838-ae81-463d-8aa5-827071f58747">DeletePolicyReader</a>
</td>
<td align="left" width="63%">
Removes the specified SID in text form from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e65af2a2-c7f7-483c-af05-342075218158">DeletePolicyReaderName</a>
</td>
<td align="left" width="63%">
Removes the specified account name from the list of principals that act as policy readers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16500d05-c5bf-4d09-8649-ebf58407120d">DeletePropertyItem</a>
</td>
<td align="left" width="63%">
Removes the specified principal from the specified  list of principals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9155c4f8-ad17-402e-80a1-3dcee044d2c4">DeleteRole</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de72b944-2796-4445-9fdd-4d56526dc903">DeleteTask</a>
</td>
<td align="left" width="63%">
Removes the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name from the <b>IAzScope</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3b5b526-5662-4971-8ba2-663e4b2c36ff">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzScope</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c0e2832-e46b-428e-8f0b-ca1d816afaeb">OpenApplicationGroup</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55ec166e-5aad-411d-8cc4-0d789c8397c4">OpenRole</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8719ab1f-8004-4d5c-b64c-ae17c8d1ab30">OpenTask</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4df2d9ca-a77f-4b32-a4e2-56ecd2059b49">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the specified value to the <b>AzScope</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c06f1994-71d9-4867-a5ed-8fa90206994f">Submit</a>
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

<a href="https://msdn.microsoft.com/c54aaadb-0c4a-43f9-ac50-413ed190b365">ApplicationData</a>


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

<a href="https://msdn.microsoft.com/a8c9cffa-aebb-4bb1-834b-338082a9c8de">ApplicationGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/e96c4cae-0a0a-4ac4-805f-2042312f0267">IAzApplicationGroups</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7cd84e64-ef90-48ca-8da0-88ca6d79e1bf">BizrulesWritable</a>


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

<a href="https://msdn.microsoft.com/e68bd5b2-060b-478b-9375-b23761888e6a">CanBeDelegated</a>


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

<a href="https://msdn.microsoft.com/51a7daff-ecb9-4a66-a7f7-aee9aeff7d6a">Description</a>


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

<a href="https://msdn.microsoft.com/66c5722a-5217-4e77-b14f-f9cfa4e030c0">Name</a>


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

<a href="https://msdn.microsoft.com/13c11105-b44d-46e0-ab73-c11fede1507b">PolicyAdministrators</a>


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

<a href="https://msdn.microsoft.com/291aa2f8-f08e-45f5-ade7-b456c962dd3f">PolicyAdministratorsName</a>


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

<a href="https://msdn.microsoft.com/7576997c-a585-4f0d-bec5-c616d39633f9">PolicyReaders</a>


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

<a href="https://msdn.microsoft.com/4f56ee3f-f987-4569-9e19-c13ab3ff100a">PolicyReadersName</a>


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

<a href="https://msdn.microsoft.com/4dcf0e1b-d824-4675-b2d1-f59a58adb00a">Roles</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/bc69ec52-ea73-4a0c-a9a2-913a6725489e">IAzRoles</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4b8a5280-570d-46eb-a6cb-2723cde3eb15">Tasks</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/324dec16-3fd6-4289-ba15-002e8626dec8">IAzTasks</a> object that is used to enumerate groups from the policy data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8e382af1-192f-4530-82a0-434f66eac060">Writable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the scope can be modified by the  user context that initialized it.

</td>
</tr>
</table> 

