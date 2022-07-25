---
UID: NN:aclui.ISecurityObjectTypeInfo
title: ISecurityObjectTypeInfo (aclui.h)
description: Provides a means of determining the source of inherited access control entries (ACEs) in discretionary access control lists (DACLs) and system access control lists (SACLs).
helpviewer_keywords: ["ISecurityObjectTypeInfo","ISecurityObjectTypeInfo interface [Security]","ISecurityObjectTypeInfo interface [Security]","described","aclui/ISecurityObjectTypeInfo","security.isecurityobjecttypeinfo"]
old-location: security\isecurityobjecttypeinfo.htm
tech.root: security
ms.assetid: 345c66b9-fa8a-4adc-a929-39bddca6aeec
ms.date: 12/05/2018
ms.keywords: ISecurityObjectTypeInfo, ISecurityObjectTypeInfo interface [Security], ISecurityObjectTypeInfo interface [Security],described, aclui/ISecurityObjectTypeInfo, security.isecurityobjecttypeinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityObjectTypeInfo
 - aclui/ISecurityObjectTypeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityObjectTypeInfo
---

# ISecurityObjectTypeInfo interface


## -description

The <b>ISecurityObjectTypeInfo</b> interface provides a means of determining the source of inherited <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in <a href="/windows/desktop/SecGloss/d-gly">discretionary access control lists</a> (DACLs) and <a href="/windows/desktop/SecGloss/s-gly">system access control lists</a> (SACLs).  The access control editor uses this information to communicate the inheritance source to the client.

## -inheritance

The <b>ISecurityObjectTypeInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityObjectTypeInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/aclui/nn-aclui-ieffectivepermission">IEffectivePermission</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>
