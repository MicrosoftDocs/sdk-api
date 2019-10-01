---
UID: NN:aclui.ISecurityObjectTypeInfo
title: ISecurityObjectTypeInfo (aclui.h)
author: windows-sdk-content
description: Provides a means of determining the source of inherited access control entries (ACEs) in discretionary access control lists (DACLs) and system access control lists (SACLs).
old-location: security\isecurityobjecttypeinfo.htm
tech.root: SecAuthZ
ms.assetid: 345c66b9-fa8a-4adc-a929-39bddca6aeec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISecurityObjectTypeInfo, ISecurityObjectTypeInfo interface [Security], ISecurityObjectTypeInfo interface [Security],described, aclui/ISecurityObjectTypeInfo, security.isecurityobjecttypeinfo
ms.topic: interface
f1_keywords: 
 - "aclui/ISecurityObjectTypeInfo"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityObjectTypeInfo interface


## -description


The <b>ISecurityObjectTypeInfo</b> interface provides a means of determining the source of inherited <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">discretionary access control lists</a> (DACLs) and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">system access control lists</a> (SACLs).  The access control editor uses this information to communicate the inheritance source to the client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityObjectTypeInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityObjectTypeInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nf-aclui-isecurityobjecttypeinfo-getinheritsource">GetInheritSource</a>
</td>
<td align="left" width="63%">
Returns the inheritance source for the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nn-aclui-ieffectivepermission">IEffectivePermission</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>
 

 

