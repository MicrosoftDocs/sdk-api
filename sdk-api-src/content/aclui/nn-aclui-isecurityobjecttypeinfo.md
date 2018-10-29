---
UID: NN:aclui.ISecurityObjectTypeInfo
title: ISecurityObjectTypeInfo
author: windows-sdk-content
description: Provides a means of determining the source of inherited access control entries (ACEs) in discretionary access control lists (DACLs) and system access control lists (SACLs).
old-location: security\isecurityobjecttypeinfo.htm
tech.root: SecAuthZ
ms.assetid: 345c66b9-fa8a-4adc-a929-39bddca6aeec
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ISecurityObjectTypeInfo, ISecurityObjectTypeInfo interface [Security], ISecurityObjectTypeInfo interface [Security],described, aclui/ISecurityObjectTypeInfo, security.isecurityobjecttypeinfo
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
 - ISecurityObjectTypeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityObjectTypeInfo interface


## -description


The <b>ISecurityObjectTypeInfo</b> interface provides a means of determining the source of inherited <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control lists</a> (DACLs) and <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control lists</a> (SACLs).  The access control editor uses this information to communicate the inheritance source to the client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityObjectTypeInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISecurityObjectTypeInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityObjectTypeInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e058ca98-08dc-4a3f-9521-adcc5990eae7">GetInheritSource</a>
</td>
<td align="left" width="63%">
Returns the inheritance source for the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c2897dad-647c-4dc1-b962-bd7fbae2da3a">IEffectivePermission</a>



<a href="https://msdn.microsoft.com/5cb7a096-5088-424a-82d1-0351ce5bb413">ISecurityInformation2</a>
 

 

