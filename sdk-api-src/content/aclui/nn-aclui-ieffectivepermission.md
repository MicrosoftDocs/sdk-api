---
UID: NN:aclui.IEffectivePermission
title: IEffectivePermission
author: windows-sdk-content
description: Provides a means to determine effective permission for a security principal on an object.
old-location: security\ieffectivepermission.htm
tech.root: SecAuthZ
ms.assetid: c2897dad-647c-4dc1-b962-bd7fbae2da3a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEffectivePermission, IEffectivePermission interface [Security], IEffectivePermission interface [Security],described, aclui/IEffectivePermission, security.ieffectivepermission
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
 - IEffectivePermission
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEffectivePermission interface


## -description


The <b>IEffectivePermission</b> interface provides a means to determine effective permission for a security principal on an object. The access control editor uses this information to communicate the effective permission to the client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEffectivePermission</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEffectivePermission</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fef2dfe0-3c56-4502-9e8d-900aea84318b">GetEffectivePermission</a>
</td>
<td align="left" width="63%">
Returns the effective permission for an object type.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5cb7a096-5088-424a-82d1-0351ce5bb413">ISecurityInformation2</a>



<a href="https://msdn.microsoft.com/345c66b9-fa8a-4adc-a929-39bddca6aeec">ISecurityObjectTypeInfo</a>
 

 

