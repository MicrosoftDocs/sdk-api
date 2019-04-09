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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation3 interface


## -description


The <b>ISecurityInformation3</b> interface provides methods necessary for displaying an elevated access control editor when a user clicks the <b>Edit</b> button on an access control editor page that displays an image of a shield on that <b>Edit</b> button. The image of a shield is displayed on the <b>Edit</b> button when the access control editor is launched by a process with a token that lacks permission to save changes to the object being edited.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityInformation3</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISecurityInformation3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a22b9a75-6aa8-4b32-8d86-7fb21afd248f">GetFullResourceName</a>
</td>
<td align="left" width="63%">
Retrieves the full path and file name of the object associated with the access control editor that is displayed by calling the <a href="https://msdn.microsoft.com/4ed50e6b-4c4a-48bf-ad7c-133064a4be47">OpenElevatedEditor</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ed50e6b-4c4a-48bf-ad7c-133064a4be47">OpenElevatedEditor</a>
</td>
<td align="left" width="63%">
Opens an access control editor when a user clicks the <b>Edit</b> button on an access control editor page that displays an image of a shield on that <b>Edit</b> button.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/5cb7a096-5088-424a-82d1-0351ce5bb413">ISecurityInformation2</a>
 

 

