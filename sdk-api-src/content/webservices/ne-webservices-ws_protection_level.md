---
UID: NE:webservices.__unnamed_enum_60
title: WS_PROTECTION_LEVEL (webservices.h)
description: Defines the required integrity and confidentiality levels for sent and received messages.
helpviewer_keywords: ["WS_PROTECTION_LEVEL","WS_PROTECTION_LEVEL enumeration [Web Services for Windows]","WS_PROTECTION_LEVEL_NONE","WS_PROTECTION_LEVEL_SIGN","WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT","webservices/WS_PROTECTION_LEVEL","webservices/WS_PROTECTION_LEVEL_NONE","webservices/WS_PROTECTION_LEVEL_SIGN","webservices/WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT","wsw.ws_protection_level"]
old-location: wsw\ws_protection_level.htm
tech.root: wsw
ms.assetid: 2b673728-1050-4005-bbb6-64b81ec19174
ms.date: 12/05/2018
ms.keywords: WS_PROTECTION_LEVEL, WS_PROTECTION_LEVEL enumeration [Web Services for Windows], WS_PROTECTION_LEVEL_NONE, WS_PROTECTION_LEVEL_SIGN, WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT, webservices/WS_PROTECTION_LEVEL, webservices/WS_PROTECTION_LEVEL_NONE, webservices/WS_PROTECTION_LEVEL_SIGN, webservices/WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT, wsw.ws_protection_level
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_PROTECTION_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_PROTECTION_LEVEL
 - webservices/WS_PROTECTION_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_PROTECTION_LEVEL
---

# WS_PROTECTION_LEVEL enumeration


## -description

Defines the required integrity and confidentiality levels for sent and
received messages.  With transport and mixed-mode security bindings,
this setting applies to each message as a whole.  With message
security, the protection level is specified at the granularity of a
message header or body.  The default value defined applies only to
transport and mixed-mode security.

## -enum-fields

### -field WS_PROTECTION_LEVEL_NONE:1

No signing or encryption.

### -field WS_PROTECTION_LEVEL_SIGN:2

Only signing.

### -field WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT:3

Signing and encryption.

