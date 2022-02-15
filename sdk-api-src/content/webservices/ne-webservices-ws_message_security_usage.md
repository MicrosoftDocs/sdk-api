---
UID: NE:webservices.__unnamed_enum_75
title: WS_MESSAGE_SECURITY_USAGE (webservices.h)
description: Defines how a message security binding attaches the security token corresponding to it to a message using WS-Security mechanisms.
helpviewer_keywords: ["WS_MESSAGE_SECURITY_USAGE","WS_MESSAGE_SECURITY_USAGE enumeration [Web Services for Windows]","WS_SUPPORTING_MESSAGE_SECURITY_USAGE","webservices/WS_MESSAGE_SECURITY_USAGE","webservices/WS_SUPPORTING_MESSAGE_SECURITY_USAGE","wsw.ws_message_security_usage"]
old-location: wsw\ws_message_security_usage.htm
tech.root: wsw
ms.assetid: 2f19877f-b79b-43c3-a3f5-93dd2940d499
ms.date: 12/05/2018
ms.keywords: WS_MESSAGE_SECURITY_USAGE, WS_MESSAGE_SECURITY_USAGE enumeration [Web Services for Windows], WS_SUPPORTING_MESSAGE_SECURITY_USAGE, webservices/WS_MESSAGE_SECURITY_USAGE, webservices/WS_SUPPORTING_MESSAGE_SECURITY_USAGE, wsw.ws_message_security_usage
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
req.typenames: WS_MESSAGE_SECURITY_USAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_MESSAGE_SECURITY_USAGE
 - webservices/WS_MESSAGE_SECURITY_USAGE
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
 - WS_MESSAGE_SECURITY_USAGE
---

# WS_MESSAGE_SECURITY_USAGE enumeration


## -description

Defines how a message security binding attaches the security token
corresponding to it to a message using WS-Security mechanisms.

## -enum-fields

### -field WS_SUPPORTING_MESSAGE_SECURITY_USAGE:1

The security token obtained security binding is used for client
authentication, but not message protection.  Message protection should
be provided by a transport security binding or a message security
binding with symmetric or asymmetric usage.

