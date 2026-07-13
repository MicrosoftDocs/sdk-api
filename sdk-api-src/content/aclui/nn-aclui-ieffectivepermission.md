---
UID: NN:aclui.IEffectivePermission
title: IEffectivePermission (aclui.h)
description: Provides a means to determine effective permission for a security principal on an object.
helpviewer_keywords: ["IEffectivePermission","IEffectivePermission interface [Security]","IEffectivePermission interface [Security]","described","aclui/IEffectivePermission","security.ieffectivepermission"]
old-location: security\ieffectivepermission.htm
tech.root: security
ms.assetid: c2897dad-647c-4dc1-b962-bd7fbae2da3a
ms.date: 12/05/2018
ms.keywords: IEffectivePermission, IEffectivePermission interface [Security], IEffectivePermission interface [Security],described, aclui/IEffectivePermission, security.ieffectivepermission
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
 - IEffectivePermission
 - aclui/IEffectivePermission
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
 - IEffectivePermission
---

# IEffectivePermission interface


## -description

The <b>IEffectivePermission</b> interface provides a means to determine effective permission for a security principal on an object. The access control editor uses this information to communicate the effective permission to the client.

## -inheritance

The <b>IEffectivePermission</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEffectivePermission</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityobjecttypeinfo">ISecurityObjectTypeInfo</a>
