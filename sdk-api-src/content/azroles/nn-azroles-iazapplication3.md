---
UID: NN:azroles.IAzApplication3
title: IAzApplication3
author: windows-sdk-content
description: Provides methods to manage IAzRoleAssignment, IAzRoleDefinition, and IAzScope2 objects.
old-location: security\iazapplication3.htm
old-project: secauthz
ms.assetid: 9d0b2c3b-b8b6-4fae-9308-9dd29da0724f
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: IAzApplication3, IAzApplication3 interface [Security], IAzApplication3 interface [Security],described, azroles/IAzApplication3, security.iazapplication3
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
 - IAzApplication3
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication3 interface


## -description


The <b>IAzApplication3</b> interface provides methods to manage <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a>, <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a>, and <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplication3</b> interface inherits from <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a>. <b>IAzApplication3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzApplication3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0646601d-97e6-437a-abfe-99fdb5bb1354">CreateRoleAssignment</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/014410be-4b2c-452b-b671-0a9bd9c0a448">CreateRoleDefinition</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1e8bfe6-e074-4e9e-80f8-bcb8bd90f824">CreateScope2</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1844e7c5-91ad-4f6d-8f5b-1a174e9653dd">DeleteRoleAssignment</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object from the <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34dc0bb8-1a44-418a-9b2c-f506f21f6ab1">DeleteRoleDefinition</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object from the <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f42f9288-896b-4034-a16c-3d555acea453">DeleteScope2</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object from the <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d0ec47e-5d5f-43d7-aace-fffca0037ac3">OpenRoleAssignment</a>
</td>
<td align="left" width="63%">
Opens the specified <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/460b917c-a07b-4f50-b80f-0f6d986b65ff">OpenRoleDefinition</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ea9f12e-d00d-4ccd-bfd4-21027610e681">OpenScope2</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/585f8b16-e634-4ac6-a20a-214eea344b0a">ScopeExists</a>
</td>
<td align="left" width="63%">
Indicates whether the scope with the specified name exists in the <b>IAzApplication3</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplication3</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/92303a5d-a705-4003-890e-e75886451c18">BizRulesEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates whether business rules are enabled for the current <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5f70cc85-9275-4ccd-ad53-c22b00a4dea3">RoleAssignments</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/d38fd7e0-6d0b-4b68-b6e5-f7adc2cfef47">IAzRoleAssignments</a> object that represents the collection of <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> objects associated with the current <b>IAzApplication3</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9b17c315-4a46-4a74-983f-b07593ff0517">RoleDefinitions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/9d17647c-3ff9-4881-a02f-d7bcb508e102">IAzRoleDefinitions</a> object that represents the collection of <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> objects associated with the current <b>IAzApplication3</b> object.

</td>
</tr>
</table> 

