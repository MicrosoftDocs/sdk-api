---
UID: NN:aclui.ISecurityInformation4
title: ISecurityInformation4 (aclui.h)
author: windows-sdk-content
description: Enables the access control editor (ACE) to obtain the share's security descriptor to initialize the share page.
old-location: security\isecurityinformation4.htm
tech.root: SecAuthZ
ms.assetid: F7AD3612-5D66-49DB-81EF-040849D32CB4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISecurityInformation4, ISecurityInformation4 interface [Security], ISecurityInformation4 interface [Security],described, aclui/ISecurityInformation4, security.isecurityinformation4
ms.topic: interface
req.header: aclui.h
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
 - ISecurityInformation4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityInformation4 interface


## -description


The <b>ISecurityInformation4</b> interface enables the resource manager to provide additional information when computing effective permissions using the <a href="https://msdn.microsoft.com/2FDCA205-6880-4526-B8D7-6F9B107B218B">IEffectivePermission2</a> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityInformation4</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISecurityInformation4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityInformation4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20BD7D3B-1097-45CF-8237-0FBAD6BD6E3E">GetSecondarySecurity</a>
</td>
<td align="left" width="63%">
Returns additional security contexts that may impact access to the resource.

</td>
</tr>
</table> 

