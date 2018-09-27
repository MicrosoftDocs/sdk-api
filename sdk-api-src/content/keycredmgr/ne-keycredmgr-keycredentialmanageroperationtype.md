---
UID: NE:keycredmgr.KeyCredentialManagerOperationType
title: KeyCredentialManagerOperationType
author: windows-sdk-content
description: These are the operational enum values that are passed to KeyCredentialManagerShowUIOperation.
old-location: security\keycredentialmanageroperationtype.htm
tech.root: secauthn
ms.assetid: 871DA6A2-0033-4863-B37E-C75ADD512C3A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: KeyCredentialManagerOperationType, KeyCredentialManagerOperationType enumeration [Security], KeyCredentialManagerPinChange, KeyCredentialManagerPinReset, KeyCredentialManagerProvisioning, keycredmgr/KeyCredentialManagerOperationType, keycredmgr/KeyCredentialManagerPinChange, keycredmgr/KeyCredentialManagerPinReset, keycredmgr/KeyCredentialManagerProvisioning, security.keycredentialmanageroperationtype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: KeyCredentialManagerOperationType
req.redist: 
---

# KeyCredentialManagerOperationType enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

These are the operational enum values that are passed to <a href="security.keycredentialmanagershowuioperation">KeyCredentialManagerShowUIOperation</a>.


## -enum-fields




### -field KeyCredentialManagerProvisioning

Start the Provisioning operation.


### -field KeyCredentialManagerPinChange

Start the User Change PIN operation.


### -field KeyCredentialManagerPinReset

Start the User PIN Reset operation.

