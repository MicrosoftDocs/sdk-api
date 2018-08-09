---
UID: NE:webservices.WS_SECURITY_TIMESTAMP_USAGE
title: WS_SECURITY_TIMESTAMP_USAGE
author: windows-sdk-content
description: With message security and mixed-mode security, this defines when a timestamp element should be generated and demanded in the WS-Security header.
old-location: wsw\ws_security_timestamp_usage.htm
old-project: wsw
ms.assetid: 72e2a404-7988-40b8-b9ec-f9b9b3d767c1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_SECURITY_TIMESTAMP_USAGE, WS_SECURITY_TIMESTAMP_USAGE enumeration [Web Services for Windows], WS_SECURITY_TIMESTAMP_USAGE_ALWAYS, WS_SECURITY_TIMESTAMP_USAGE_NEVER, WS_SECURITY_TIMESTAMP_USAGE_REQUESTS_ONLY, webservices/WS_SECURITY_TIMESTAMP_USAGE, webservices/WS_SECURITY_TIMESTAMP_USAGE_ALWAYS, webservices/WS_SECURITY_TIMESTAMP_USAGE_NEVER, webservices/WS_SECURITY_TIMESTAMP_USAGE_REQUESTS_ONLY, wsw.ws_security_timestamp_usage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WS_SECURITY_TIMESTAMP_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_TIMESTAMP_USAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SECURITY_TIMESTAMP_USAGE enumeration


## -description


With message security and mixed-mode security, this defines when a
timestamp element should be generated and demanded in the WS-Security
header.
            


## -enum-fields




### -field WS_SECURITY_TIMESTAMP_USAGE_ALWAYS

Always generate a timestamp in each outgoing message and demand a
timestamp be present in each incoming message, whether those messages
are requests or replies.
                


### -field WS_SECURITY_TIMESTAMP_USAGE_NEVER

Do not use timestamps in requests or replies.  It is an error to
specify this value when a mixed-mode message signature is required in
the WS-Security header.
                


### -field WS_SECURITY_TIMESTAMP_USAGE_REQUESTS_ONLY

Generate and demand timestamps in client to server request messages,
but not in server to client reply messages.  This value may be used in
mixed-mode security.
                

