---
UID: NS:subauth._SR_SECURITY_DESCRIPTOR
title: SR_SECURITY_DESCRIPTOR (subauth.h)
description: The SR_SECURITY_DESCRIPTOR structure contains information about the security privileges of the user.
helpviewer_keywords: ["*PSR_SECURITY_DESCRIPTOR","PSR_SECURITY_DESCRIPTOR","PSR_SECURITY_DESCRIPTOR structure pointer [Security]","SR_SECURITY_DESCRIPTOR","SR_SECURITY_DESCRIPTOR structure [Security]","_lsa_sr_security_descriptor","security.sr_security_descriptor","subauth/PSR_SECURITY_DESCRIPTOR","subauth/SR_SECURITY_DESCRIPTOR"]
old-location: security\sr_security_descriptor.htm
tech.root: security
ms.assetid: 000ffbbe-5750-449b-8237-27c8d3c45454
ms.date: 12/05/2018
ms.keywords: '*PSR_SECURITY_DESCRIPTOR, PSR_SECURITY_DESCRIPTOR, PSR_SECURITY_DESCRIPTOR structure pointer [Security], SR_SECURITY_DESCRIPTOR, SR_SECURITY_DESCRIPTOR structure [Security], _lsa_sr_security_descriptor, security.sr_security_descriptor, subauth/PSR_SECURITY_DESCRIPTOR, subauth/SR_SECURITY_DESCRIPTOR'
req.header: subauth.h
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
req.typenames: SR_SECURITY_DESCRIPTOR, *PSR_SECURITY_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SR_SECURITY_DESCRIPTOR
 - subauth/_SR_SECURITY_DESCRIPTOR
 - PSR_SECURITY_DESCRIPTOR
 - subauth/PSR_SECURITY_DESCRIPTOR
 - SR_SECURITY_DESCRIPTOR
 - subauth/SR_SECURITY_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Subauth.h
api_name:
 - SR_SECURITY_DESCRIPTOR
---

# SR_SECURITY_DESCRIPTOR structure


## -description

The <b>SR_SECURITY_DESCRIPTOR</b> structure contains information about the security <a href="/windows/desktop/SecGloss/p-gly">privileges</a> of the user.

## -struct-fields

### -field Length

Indicates the size in bytes of the structure.

### -field SecurityDescriptor

Indicates the user's security privileges.