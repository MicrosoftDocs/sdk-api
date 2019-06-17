---
UID: NN:aclui.IEffectivePermission
title: IEffectivePermission (aclui.h)
author: windows-sdk-content
description: Provides a means to determine effective permission for a security principal on an object.
old-location: security\ieffectivepermission.htm
tech.root: SecAuthZ
ms.assetid: c2897dad-647c-4dc1-b962-bd7fbae2da3a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEffectivePermission, IEffectivePermission interface [Security], IEffectivePermission interface [Security],described, aclui/IEffectivePermission, security.ieffectivepermission
ms.topic: interface
f1_keywords: ["aclui/IEffectivePermission"]
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
 - IEffectivePermission
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEffectivePermission interface


## -description


The <b>IEffectivePermission</b> interface provides a means to determine effective permission for a security principal on an object. The access control editor uses this information to communicate the effective permission to the client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEffectivePermission</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEffectivePermission</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEffectivePermission</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-ieffectivepermission-geteffectivepermission">GetEffectivePermission</a>
</td>
<td align="left" width="63%">
Returns the effective permission for an object type.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nn-aclui-isecurityobjecttypeinfo">ISecurityObjectTypeInfo</a>
 

 

