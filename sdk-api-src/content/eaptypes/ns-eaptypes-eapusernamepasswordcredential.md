---
UID: NS:eaptypes._EapUsernamePasswordCredential
title: EapUsernamePasswordCredential
description: Contains the username and password that is used by the EAP method for authenticating the user.
helpviewer_keywords: ["_EapUsernamePasswordCredential","EapUsernamePasswordCredential"]
old-location: eaphost\eapusernamepasswordcredential.htm
tech.root: eaphost
ms.assetid: 61484095-4354-4103-9E21-683002750B26
ms.date: 12/05/2018
ms.keywords: _EapUsernamePasswordCredential, EapUsernamePasswordCredential
req.construct-type: structure
req.header: eaptypes.h
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
req.typenames: EapUsernamePasswordCredential
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EapUsernamePasswordCredential
 - eaptypes/_EapUsernamePasswordCredential
 - EapUsernamePasswordCredential
 - eaptypes/EapUsernamePasswordCredential
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - _EapUsernamePasswordCredential
 - EapUsernamePasswordCredential
---

# EapUsernamePasswordCredential structure


## -description

The **EapUsernamePasswordCredential** structure contains the username and password that is used by the EAP method for authenticating the user.

## -struct-fields

### -field username

A NULL-terminated Unicode string that contains the username that needs authentication. The username uses the format user@domain or domain\user.

### -field password

A NULL-terminated Unicode string that contains the password to verify the user. The password is encrypted using the [CredProtect](../wincred/nf-wincred-credprotectw.md) function. The EAP method must use the [CredUnprotect](../wincred/nf-wincred-credunprotecta.md) function to retrieve the unencrypted password.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential">EapCredential</a>
<a href="/windows/desktop/api/eaptypes/ne-eaptypes-eapcredentialtype">EapCredentialType</a>