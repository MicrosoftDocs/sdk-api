---
UID: NN:netfw.INetFwRule3
title: INetFwRule3
author: windows-sdk-content
description: Allows an application or service to access all the properties of INetFwRule2 and to provide access to the requirements of app containers.
old-location: ics\inetfwrule3.htm
tech.root: ICS
ms.assetid: 72bf5ac3-7ee7-4837-96b2-815b499aac2f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: INetFwRule3, INetFwRule3 interface [ICS/ICF], INetFwRule3 interface [ICS/ICF],described, ics.inetfwrule3, netfw/INetFwRule3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRule3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwRule3 interface


## -description


The <b>INetFwRule3</b> interface allows an application or service to access all the properties of <a href="https://msdn.microsoft.com/35c28180-b60c-4dc1-81ce-0ce012f96525">INetFwRule2</a> and to provide access to the requirements of app containers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRule3</b> interface inherits from <b>INetFwRule2</b>. <b>INetFwRule3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwRule3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c1bccc6-3c8d-401c-8e9f-e88a4a60e3f4">get_LocalAppPackageId</a>
</td>
<td align="left" width="63%">
Retrieves the LocalAppPackageId property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a44ce34-bf0b-4a8b-a8b3-bd5e4cc3bea8">get_LocalUserAuthorizedList</a>
</td>
<td align="left" width="63%">
Retrieves the LocalUserAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5eeacde4-6e25-49dc-a8f5-77a6e56dcade">get_LocalUserOwner</a>
</td>
<td align="left" width="63%">
Retrieves the LocalUserOwner property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43acf254-594a-4d19-a9e4-bce0a188a9de">get_RemoteMachineAuthorizedList</a>
</td>
<td align="left" width="63%">
Retrieves the RemoteMachineAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9364d317-b32a-4b8d-b67a-32a34b64a5ac">get_RemoteUserAuthorizedList</a>
</td>
<td align="left" width="63%">
Retrieves the RemoteUserAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3efb3491-f030-4a0a-bfbd-ab18fd424a38">get_SecureFlags</a>
</td>
<td align="left" width="63%">
Retrieves the SecureFlags property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c1bccc6-3c8d-401c-8e9f-e88a4a60e3f4">put_LocalAppPackageId</a>
</td>
<td align="left" width="63%">
Sets the LocalAppPackageId property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a44ce34-bf0b-4a8b-a8b3-bd5e4cc3bea8">put_LocalUserAuthorizedList</a>
</td>
<td align="left" width="63%">
Sets the LocalUserAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5eeacde4-6e25-49dc-a8f5-77a6e56dcade">put_LocalUserOwner</a>
</td>
<td align="left" width="63%">
Sets the LocalUserOwner property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43acf254-594a-4d19-a9e4-bce0a188a9de">put_RemoteMachineAuthorizedList</a>
</td>
<td align="left" width="63%">
Sets the RemoteMachineAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9364d317-b32a-4b8d-b67a-32a34b64a5ac">put_RemoteUserAuthorizedList</a>
</td>
<td align="left" width="63%">
Sets the RemoteUserAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3efb3491-f030-4a0a-bfbd-ab18fd424a38">put_SecureFlags</a>
</td>
<td align="left" width="63%">
Sets the SecureFlags property for this rule.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRule3</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8c1bccc6-3c8d-401c-8e9f-e88a4a60e3f4">LocalAppPackageId</a>


</td>
<td align="left" width="63%">
Accesses the LocalAppPackageId property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5a44ce34-bf0b-4a8b-a8b3-bd5e4cc3bea8">LocalUserAuthorizedList</a>


</td>
<td align="left" width="63%">
Accesses the LocalUserAuthorizedList property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5eeacde4-6e25-49dc-a8f5-77a6e56dcade">LocalUserOwner</a>


</td>
<td align="left" width="63%">
Accesses the LocalUserOwner property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/43acf254-594a-4d19-a9e4-bce0a188a9de">RemoteMachineAuthorizedList</a>


</td>
<td align="left" width="63%">
Accesses the RemoteMachineAuthorizedList property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9364d317-b32a-4b8d-b67a-32a34b64a5ac">RemoteUserAuthorizedList</a>


</td>
<td align="left" width="63%">
Accesses the RemoteUserAuthorizedList property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3efb3491-f030-4a0a-bfbd-ab18fd424a38">SecureFlags</a>


</td>
<td align="left" width="63%">
Accesses the SecureFlags property of this rule.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/35c28180-b60c-4dc1-81ce-0ce012f96525">INetFwRule2</a>
 

 

