---
UID: NE:webservices.__unnamed_enum_62
title: WS_SECURITY_KEY_TYPE (webservices.h)
description: The key type of a security token. It is used as the return type when a security token is queried about its key. It is also used to specify the required key type when requesting a security token from a security token service.
helpviewer_keywords: ["WS_SECURITY_KEY_TYPE","WS_SECURITY_KEY_TYPE enumeration [Web Services for Windows]","WS_SECURITY_KEY_TYPE_ASYMMETRIC","WS_SECURITY_KEY_TYPE_NONE","WS_SECURITY_KEY_TYPE_SYMMETRIC","webservices/WS_SECURITY_KEY_TYPE","webservices/WS_SECURITY_KEY_TYPE_ASYMMETRIC","webservices/WS_SECURITY_KEY_TYPE_NONE","webservices/WS_SECURITY_KEY_TYPE_SYMMETRIC","wsw.ws_security_key_type"]
old-location: wsw\ws_security_key_type.htm
tech.root: wsw
ms.assetid: 95915a10-ba8f-41ca-89eb-777c85d2a411
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_KEY_TYPE, WS_SECURITY_KEY_TYPE enumeration [Web Services for Windows], WS_SECURITY_KEY_TYPE_ASYMMETRIC, WS_SECURITY_KEY_TYPE_NONE, WS_SECURITY_KEY_TYPE_SYMMETRIC, webservices/WS_SECURITY_KEY_TYPE, webservices/WS_SECURITY_KEY_TYPE_ASYMMETRIC, webservices/WS_SECURITY_KEY_TYPE_NONE, webservices/WS_SECURITY_KEY_TYPE_SYMMETRIC, wsw.ws_security_key_type
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
req.typenames: WS_SECURITY_KEY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_KEY_TYPE
 - webservices/WS_SECURITY_KEY_TYPE
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
 - WS_SECURITY_KEY_TYPE
---

# WS_SECURITY_KEY_TYPE enumeration


## -description

The key type of a security token.  It is used as the return type when
a security token is queried about its key.  It is also used to specify
the required key type when requesting a security token from a security
token service.

## -enum-fields

### -field WS_SECURITY_KEY_TYPE_NONE:1

Has no key -- it may be a bearer token such as a username/password
pair.

### -field WS_SECURITY_KEY_TYPE_SYMMETRIC:2

Has a symmetric key.

### -field WS_SECURITY_KEY_TYPE_ASYMMETRIC:3

Has an asymmetric key.

