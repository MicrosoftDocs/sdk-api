---
UID: NN:aclui.IEffectivePermission2
title: IEffectivePermission2
author: windows-sdk-content
description: Provides a way to determine effective permission for a security principal on an object.
old-location: security\ieffectivepermission2.htm
tech.root: secauthz
ms.assetid: 2FDCA205-6880-4526-B8D7-6F9B107B218B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEffectivePermission2, IEffectivePermission2 interface [Security], IEffectivePermission2 interface [Security],described, aclui/IEffectivePermission2, security.ieffectivepermission2
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
 - IEffectivePermission2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEffectivePermission2 interface


## -description


The <b>IEffectivePermission2</b> interface provides a way to determine effective permissions for a security principal on an object in a way where the principal's security context may be compounded with a device context or adjusted in other ways. Additionally, it determines the effective permissions even when multiple security checks apply. The access control editor uses this information to communicate the effective permissions to the client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEffectivePermission2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEffectivePermission2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEffectivePermission2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03B73103-D7C0-4BA2-B315-3CC0049B1B8E">ComputeEffectivePermissionWithSecondarySecurity</a>
</td>
<td align="left" width="63%">
Computes the effective permissions by using the secondary security for an object.

</td>
</tr>
</table> 


## -remarks



The <b>IEffectivePermission2</b> interface should be implemented by resource managers that support dynamic access control or by resource managers where the effective access to an object is determined by more than one security check, for example, a security descriptor and a firewall. 

The resource manager typically implements <a href="https://msdn.microsoft.com/F7AD3612-5D66-49DB-81EF-040849D32CB4">ISecurityInformation4</a> before implementing <b>IEffectivePermission2</b> because <b>IEffectivePermission2</b> interprets the <a href="https://msdn.microsoft.com/C3E61527-76AB-49E9-8BBD-486F437CC677">SECURITY_OBJECT</a> returned by the <a href="https://msdn.microsoft.com/20BD7D3B-1097-45CF-8237-0FBAD6BD6E3E">GetSecondarySecurity</a> method.

If the <b>IEffectivePermission2</b> interface is implemented, then the <a href="https://msdn.microsoft.com/c2897dad-647c-4dc1-b962-bd7fbae2da3a">IEffectivePermission</a> interface is not used.




## -see-also




<a href="https://msdn.microsoft.com/c2897dad-647c-4dc1-b962-bd7fbae2da3a">IEffectivePermission</a>
 

 

