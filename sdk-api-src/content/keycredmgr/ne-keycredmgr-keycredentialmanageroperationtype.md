---
UID: NE:keycredmgr.KeyCredentialManagerOperationType
title: KeyCredentialManagerOperationType (keycredmgr.h)
description: These are the operational enum values that are passed to KeyCredentialManagerShowUIOperation.
helpviewer_keywords: ["KeyCredentialManagerOperationType","KeyCredentialManagerOperationType enumeration [Security]","KeyCredentialManagerPinChange","KeyCredentialManagerPinReset","KeyCredentialManagerProvisioning","keycredmgr/KeyCredentialManagerOperationType","keycredmgr/KeyCredentialManagerPinChange","keycredmgr/KeyCredentialManagerPinReset","keycredmgr/KeyCredentialManagerProvisioning","security.keycredentialmanageroperationtype"]
old-location: security\keycredentialmanageroperationtype.htm
tech.root: SecAuthN
ms.assetid: 871DA6A2-0033-4863-B37E-C75ADD512C3A
ms.date: 12/05/2018
ms.keywords: KeyCredentialManagerOperationType, KeyCredentialManagerOperationType enumeration [Security], KeyCredentialManagerPinChange, KeyCredentialManagerPinReset, KeyCredentialManagerProvisioning, keycredmgr/KeyCredentialManagerOperationType, keycredmgr/KeyCredentialManagerPinChange, keycredmgr/KeyCredentialManagerPinReset, keycredmgr/KeyCredentialManagerProvisioning, security.keycredentialmanageroperationtype
f1_keywords:
- keycredmgr/KeyCredentialManagerOperationType
dev_langs:
- c++
req.header: keycredmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- HeaderDef
api_location:
- keycredmgr.h
api_name:
- KeyCredentialManagerOperationType
targetos: Windows
req.typenames: KeyCredentialManagerOperationType
req.redist: 
ms.custom: 19H1
---

# KeyCredentialManagerOperationType enumeration


## -description


These are the operational enum values that are passed to <a href="https://msdn.microsoft.com/en-us/library/Mt830292(v=VS.85).aspx">KeyCredentialManagerShowUIOperation</a>.


## -enum-fields




### -field KeyCredentialManagerProvisioning

Start the Provisioning operation.


### -field KeyCredentialManagerPinChange

Start the User Change PIN operation.


### -field KeyCredentialManagerPinReset

Start the User PIN Reset operation.

