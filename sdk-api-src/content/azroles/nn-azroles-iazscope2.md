---
UID: NN:azroles.IAzScope2
title: IAzScope2
author: windows-sdk-content
description: Extends the IAzScope interface to manage IAzRoleAssignment and IAzRoleDefinition objects.
old-location: security\iazscope2.htm
tech.root: SecAuthZ
ms.assetid: 536c563e-7a6b-480d-9e83-1d7cc90a795d
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: IAzScope2, IAzScope2 interface [Security], IAzScope2 interface [Security],described, azroles/IAzScope2, security.iazscope2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IAzScope2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzScope2 interface


## -description


The <b>IAzScope2</b> interface extends the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> interface to manage <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> and <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzScope2</b> interface inherits from <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a>. <b>IAzScope2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzScope2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98cb412b-9742-4f94-a470-61e675f6b253">CreateRoleAssignment</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object with the specified name in this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcd78233-a484-4c99-9dbb-9f559f7542a4">CreateRoleDefinition</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name in this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e28e09a-f9a4-4e6e-bb11-cfa1145f1ba1">DeleteRoleAssignment</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object from this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12eddceb-15e2-4c9a-8372-749b0eccdd79">DeleteRoleDefinition</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object from the <b>IAzScope2</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb7560d0-da5c-444d-9944-b6db980985bc">OpenRoleAssignment</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object with the specified name in this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58b792aa-1432-4b23-8d7a-33606741bf27">OpenRoleDefinition</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name in this scope.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzScope2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9f844f6b-8c31-4cec-ae72-a3fd4e947d49">RoleAssignments</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/d38fd7e0-6d0b-4b68-b6e5-f7adc2cfef47">IAzRoleAssignments</a> object that represents the collection of <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> objects associated with this scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cff40ce8-fa5f-4673-9338-58cff2c941aa">RoleDefinitions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/9d17647c-3ff9-4881-a02f-d7bcb508e102">IAzRoleDefinitions</a> object that represents the collection of <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> objects associated with this scope.

</td>
</tr>
</table> 

