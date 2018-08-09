---
UID: NE:webservices.WS_SECURITY_KEY_ENTROPY_MODE
title: WS_SECURITY_KEY_ENTROPY_MODE
author: windows-sdk-content
description: Defines how randomness should be contributed to the issued key during a security token negotiation done with message and mixed-mode security.
old-location: wsw\ws_security_key_entropy_mode.htm
old-project: wsw
ms.assetid: dd6bca9a-e47b-46b3-b9ac-23aecb101337
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_SECURITY_KEY_ENTROPY_MODE, WS_SECURITY_KEY_ENTROPY_MODE enumeration [Web Services for Windows], WS_SECURITY_KEY_ENTROPY_MODE_CLIENT_ONLY, WS_SECURITY_KEY_ENTROPY_MODE_COMBINED, WS_SECURITY_KEY_ENTROPY_MODE_SERVER_ONLY, webservices/WS_SECURITY_KEY_ENTROPY_MODE, webservices/WS_SECURITY_KEY_ENTROPY_MODE_CLIENT_ONLY, webservices/WS_SECURITY_KEY_ENTROPY_MODE_COMBINED, webservices/WS_SECURITY_KEY_ENTROPY_MODE_SERVER_ONLY, wsw.ws_security_key_entropy_mode
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
req.typenames: WS_SECURITY_KEY_ENTROPY_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_KEY_ENTROPY_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SECURITY_KEY_ENTROPY_MODE enumeration


## -description


Defines how randomness should be contributed to the issued key during
a security token negotiation done with message and mixed-mode security.
            


## -enum-fields




### -field WS_SECURITY_KEY_ENTROPY_MODE_CLIENT_ONLY

Only client contributes entropy.
                


### -field WS_SECURITY_KEY_ENTROPY_MODE_SERVER_ONLY

Only service contributes entropy.
                


### -field WS_SECURITY_KEY_ENTROPY_MODE_COMBINED

Both contribute entropy.
                

