---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
                

