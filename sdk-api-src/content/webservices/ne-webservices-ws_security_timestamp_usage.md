---
UID: NE:webservices.__unnamed_enum_56
title: WS_SECURITY_TIMESTAMP_USAGE (webservices.h)
description: With message security and mixed-mode security, this defines when a timestamp element should be generated and demanded in the WS-Security header.
helpviewer_keywords: ["WS_SECURITY_TIMESTAMP_USAGE","WS_SECURITY_TIMESTAMP_USAGE enumeration [Web Services for Windows]","WS_SECURITY_TIMESTAMP_USAGE_ALWAYS","WS_SECURITY_TIMESTAMP_USAGE_NEVER","WS_SECURITY_TIMESTAMP_USAGE_REQUESTS_ONLY","webservices/WS_SECURITY_TIMESTAMP_USAGE","webservices/WS_SECURITY_TIMESTAMP_USAGE_ALWAYS","webservices/WS_SECURITY_TIMESTAMP_USAGE_NEVER","webservices/WS_SECURITY_TIMESTAMP_USAGE_REQUESTS_ONLY","wsw.ws_security_timestamp_usage"]
old-location: wsw\ws_security_timestamp_usage.htm
tech.root: wsw
ms.assetid: 72e2a404-7988-40b8-b9ec-f9b9b3d767c1
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_TIMESTAMP_USAGE, WS_SECURITY_TIMESTAMP_USAGE enumeration [Web Services for Windows], WS_SECURITY_TIMESTAMP_USAGE_ALWAYS, WS_SECURITY_TIMESTAMP_USAGE_NEVER, WS_SECURITY_TIMESTAMP_USAGE_REQUESTS_ONLY, webservices/WS_SECURITY_TIMESTAMP_USAGE, webservices/WS_SECURITY_TIMESTAMP_USAGE_ALWAYS, webservices/WS_SECURITY_TIMESTAMP_USAGE_NEVER, webservices/WS_SECURITY_TIMESTAMP_USAGE_REQUESTS_ONLY, wsw.ws_security_timestamp_usage
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
req.typenames: WS_SECURITY_TIMESTAMP_USAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_TIMESTAMP_USAGE
 - webservices/WS_SECURITY_TIMESTAMP_USAGE
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
 - WS_SECURITY_TIMESTAMP_USAGE
---

# WS_SECURITY_TIMESTAMP_USAGE enumeration


## -description

With message security and mixed-mode security, this defines when a
timestamp element should be generated and demanded in the WS-Security
header.

## -enum-fields

### -field WS_SECURITY_TIMESTAMP_USAGE_ALWAYS:1

Always generate a timestamp in each outgoing message and demand a
timestamp be present in each incoming message, whether those messages
are requests or replies.

### -field WS_SECURITY_TIMESTAMP_USAGE_NEVER:2

Do not use timestamps in requests or replies.  It is an error to
specify this value when a mixed-mode message signature is required in
the WS-Security header.

### -field WS_SECURITY_TIMESTAMP_USAGE_REQUESTS_ONLY:3

Generate and demand timestamps in client to server request messages,
but not in server to client reply messages.  This value may be used in
mixed-mode security.

