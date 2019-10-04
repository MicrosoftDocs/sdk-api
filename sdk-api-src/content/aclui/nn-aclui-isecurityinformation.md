---
UID: NN:aclui.ISecurityInformation
title: ISecurityInformation (aclui.h)
author: windows-sdk-content
description: Enables the access control editor to communicate with the caller of the CreateSecurityPage and EditSecurity functions.
old-location: security\isecurityinformation.htm
tech.root: SecAuthZ
ms.assetid: 38d94f36-f149-4b62-a710-8f7359bfd8cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISecurityInformation, ISecurityInformation interface [Security], ISecurityInformation interface [Security],described, _win32_isecurityinformation, aclui/ISecurityInformation, security.isecurityinformation
ms.topic: interface
f1_keywords: 
 - "aclui/ISecurityInformation"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityInformation interface


## -description


The <b>ISecurityInformation</b> interface enables the access control editor to communicate with the caller of the 
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a> functions. The editor calls the interface methods to retrieve information that is used to initialize its pages and to determine the editing options available to the user. The editor also calls the interface methods to pass the user's input back to the application.

The <b>LPSECURITYINFO</b> type is a pointer to an <b>ISecurityInformation</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityInformation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityInformation</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getaccessrights">GetAccessRights</a>
</td>
<td align="left" width="63%">
Requests information about the access rights supported by the object being edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getinherittypes">GetInheritTypes</a>
</td>
<td align="left" width="63%">
Requests information about how the object's ACEs can be inherited by child objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">GetObjectInformation</a>
</td>
<td align="left" width="63%">
Requests information that is used to initialize the access control editor and to determine the editing options available to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">GetSecurity</a>
</td>
<td align="left" width="63%">
Requests the security descriptor of the object being edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation-mapgeneric">MapGeneric</a>
</td>
<td align="left" width="63%">
Requests that the generic access rights in an access mask be mapped to their corresponding standard and specific access rights.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation-propertysheetpagecallback">PropertySheetPageCallback</a>
</td>
<td align="left" width="63%">
Notifies the application that an access control editor property page is being created or destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">SetSecurity</a>
</td>
<td align="left" width="63%">
Provides a security descriptor containing the security information specified by the user.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>
 

 

