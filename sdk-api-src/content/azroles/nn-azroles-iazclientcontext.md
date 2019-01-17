---
UID: NN:azroles.IAzClientContext
title: IAzClientContext
author: windows-sdk-content
description: Maintains the state that describes a particular client.
old-location: security\iazclientcontext.htm
tech.root: SecAuthZ
ms.assetid: e24184d2-a77b-4a8b-b2f3-78f1e0b902f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAzClientContext, IAzClientContext interface [Security], IAzClientContext interface [Security],described, azroles/IAzClientContext, security.iazclientcontext
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
 - IAzClientContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzClientContext interface


## -description


The <b>IAzClientContext</b> interface maintains the state that describes a particular client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzClientContext</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAzClientContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzClientContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a>
</td>
<td align="left" width="63%">
Determines whether the current client context is allowed to perform the specified operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44cd9331-4891-45fe-9392-04c19da0ac7d">GetBusinessRuleString</a>
</td>
<td align="left" width="63%">
Returns the application-specific string for the business rule (BizRule).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4be02b6d-5eeb-46e6-9339-3edd904f3606">GetProperty</a>
</td>
<td align="left" width="63%">
Returns the <b>IAzClientContext</b> object property  with the specified property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/753506cc-ed44-4795-90e5-c76010181d8a">GetRoles</a>
</td>
<td align="left" width="63%">
Returns the roles for the client context.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzClientContext</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/817b3693-b989-431c-a8b3-bdeeb0367dc6">RoleForAccessCheck</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the role that is used to perform the access check.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/413cdbbd-a9c6-4117-9df5-d7eb202191a4">UserCanonical</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the current client in canonical format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/db75ecc1-0096-4e14-a5be-10b596ad5163">UserDisplay</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the current client in user display name format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1561352c-254e-41a2-bfc9-795a678ce180">UserDn</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the current client in distinguished name (DN) format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8f2739cd-3add-4a3c-9c00-8b23d2cec068">UserDnsSamCompat</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the current client in a DNS format compatible with Windows Security Account Manager (SAM).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fd60d1d0-67b9-457f-a01e-6ea470d9db6a">UserGuid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the current client in GUID format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3b1f9e8a-cc3b-4be6-b2d9-8e8b3164d46a">UserSamCompat</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the current client in a format compatible with SAM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e54d450b-7059-43c7-9c08-688975031401">UserUpn</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the current client in user principal name (UPN) format.

</td>
</tr>
</table> 

