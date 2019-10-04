---
UID: NN:aclui.ISecurityInformation3
title: ISecurityInformation3 (aclui.h)
author: windows-sdk-content
description: Provides methods necessary for displaying an elevated access control editor when a user clicks the Edit button on an access control editor page that displays an image of a shield on that Edit button.
old-location: security\isecurityinformation3.htm
tech.root: SecAuthZ
ms.assetid: e6cf92da-ebd2-4960-9df1-7124745df616
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISecurityInformation3, ISecurityInformation3 interface [Security], ISecurityInformation3 interface [Security],described, aclui/ISecurityInformation3, security.isecurityinformation3
ms.topic: interface
f1_keywords: 
 - "aclui/ISecurityInformation3"
dev_langs:
 - c++
req.header: aclui.h
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
 - ISecurityInformation3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityInformation3 interface


## -description


The <b>ISecurityInformation3</b> interface provides methods necessary for displaying an elevated access control editor when a user clicks the <b>Edit</b> button on an access control editor page that displays an image of a shield on that <b>Edit</b> button. The image of a shield is displayed on the <b>Edit</b> button when the access control editor is launched by a process with a token that lacks permission to save changes to the object being edited.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityInformation3</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityInformation3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityInformation3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation3-getfullresourcename">GetFullResourceName</a>
</td>
<td align="left" width="63%">
Retrieves the full path and file name of the object associated with the access control editor that is displayed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation3-openelevatededitor">OpenElevatedEditor</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityinformation3-openelevatededitor">OpenElevatedEditor</a>
</td>
<td align="left" width="63%">
Opens an access control editor when a user clicks the <b>Edit</b> button on an access control editor page that displays an image of a shield on that <b>Edit</b> button.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>
 

 

