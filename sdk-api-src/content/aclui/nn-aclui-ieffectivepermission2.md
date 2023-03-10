---
UID: NN:aclui.IEffectivePermission2
title: IEffectivePermission2 (aclui.h)
description: Provides a way to determine effective permission for a security principal on an object.
helpviewer_keywords: ["IEffectivePermission2","IEffectivePermission2 interface [Security]","IEffectivePermission2 interface [Security]","described","aclui/IEffectivePermission2","security.ieffectivepermission2"]
old-location: security\ieffectivepermission2.htm
tech.root: security
ms.assetid: 2FDCA205-6880-4526-B8D7-6F9B107B218B
ms.date: 12/05/2018
ms.keywords: IEffectivePermission2, IEffectivePermission2 interface [Security], IEffectivePermission2 interface [Security],described, aclui/IEffectivePermission2, security.ieffectivepermission2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEffectivePermission2
 - aclui/IEffectivePermission2
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
 - IEffectivePermission2
---

# IEffectivePermission2 interface


## -description

The <b>IEffectivePermission2</b> interface provides a way to determine effective permissions for a security principal on an object in a way where the principal's security context may be compounded with a device context or adjusted in other ways. Additionally, it determines the effective permissions even when multiple security checks apply. The access control editor uses this information to communicate the effective permissions to the client.

## -inheritance

The <b>IEffectivePermission2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEffectivePermission2</b> also has these types of members:

## -remarks

The <b>IEffectivePermission2</b> interface should be implemented by resource managers that support dynamic access control or by resource managers where the effective access to an object is determined by more than one security check, for example, a security descriptor and a firewall. 

The resource manager typically implements <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation4">ISecurityInformation4</a> before implementing <b>IEffectivePermission2</b> because <b>IEffectivePermission2</b> interprets the <a href="/windows/desktop/api/aclui/ns-aclui-security_object">SECURITY_OBJECT</a> returned by the <a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation4-getsecondarysecurity">GetSecondarySecurity</a> method.

If the <b>IEffectivePermission2</b> interface is implemented, then the <a href="/windows/desktop/api/aclui/nn-aclui-ieffectivepermission">IEffectivePermission</a> interface is not used.

## -see-also

<a href="/windows/desktop/api/aclui/nn-aclui-ieffectivepermission">IEffectivePermission</a>
