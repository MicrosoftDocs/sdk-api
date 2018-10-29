---
UID: NN:aclui.ISecurityInformation
title: ISecurityInformation
author: windows-sdk-content
description: Enables the access control editor to communicate with the caller of the CreateSecurityPage and EditSecurity functions.
old-location: security\isecurityinformation.htm
tech.root: SecAuthZ
ms.assetid: 38d94f36-f149-4b62-a710-8f7359bfd8cd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ISecurityInformation, ISecurityInformation interface [Security], ISecurityInformation interface [Security],described, _win32_isecurityinformation, aclui/ISecurityInformation, security.isecurityinformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation interface


## -description


The <b>ISecurityInformation</b> interface enables the access control editor to communicate with the caller of the 
<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a> and 
<a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a> functions. The editor calls the interface methods to retrieve information that is used to initialize its pages and to determine the editing options available to the user. The editor also calls the interface methods to pass the user's input back to the application.

The <b>LPSECURITYINFO</b> type is a pointer to an <b>ISecurityInformation</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISecurityInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a40b3ded-9a75-476b-bc7e-38794a98261c">GetAccessRights</a>
</td>
<td align="left" width="63%">
Requests information about the access rights supported by the object being edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dafe6c45-616f-4339-a119-9b88055b5d3a">GetInheritTypes</a>
</td>
<td align="left" width="63%">
Requests information about how the object's ACEs can be inherited by child objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bc63aa0-dada-4962-a381-6b0f8332e564">GetObjectInformation</a>
</td>
<td align="left" width="63%">
Requests information that is used to initialize the access control editor and to determine the editing options available to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c9e05fd-0b58-4d6d-b33e-067d9e8e2915">GetSecurity</a>
</td>
<td align="left" width="63%">
Requests the security descriptor of the object being edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85ad4d42-11e7-4d26-943f-3d7451899c8e">MapGeneric</a>
</td>
<td align="left" width="63%">
Requests that the generic access rights in an access mask be mapped to their corresponding standard and specific access rights.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b891e64-e648-44a4-add6-d4c214394be8">PropertySheetPageCallback</a>
</td>
<td align="left" width="63%">
Notifies the application that an access control editor property page is being created or destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c23c5ad-8088-4cfb-9746-99d24cc3bd0e">SetSecurity</a>
</td>
<td align="left" width="63%">
Provides a security descriptor containing the security information specified by the user.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a>



<a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a>



<a href="https://msdn.microsoft.com/5cb7a096-5088-424a-82d1-0351ce5bb413">ISecurityInformation2</a>
 

 

