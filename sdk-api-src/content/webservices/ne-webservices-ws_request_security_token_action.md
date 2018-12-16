---
UID: NE:webservices.__unnamed_enum_53
title: WS_REQUEST_SECURITY_TOKEN_ACTION
author: windows-sdk-content
description: Defines which set of actions to use when negotiating security tokens using WS-Trust.
old-location: wsw\ws_request_security_token_action.htm
tech.root: wsw
ms.assetid: 1ef2ab60-c0a6-461a-9c93-fce74e8d76ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_REQUEST_SECURITY_TOKEN_ACTION, WS_REQUEST_SECURITY_TOKEN_ACTION enumeration [Web Services for Windows], WS_REQUEST_SECURITY_TOKEN_ACTION_ISSUE, WS_REQUEST_SECURITY_TOKEN_ACTION_NEW_CONTEXT, WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT, webservices/WS_REQUEST_SECURITY_TOKEN_ACTION, webservices/WS_REQUEST_SECURITY_TOKEN_ACTION_ISSUE, webservices/WS_REQUEST_SECURITY_TOKEN_ACTION_NEW_CONTEXT, webservices/WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT, wsw.ws_request_security_token_action
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_REQUEST_SECURITY_TOKEN_ACTION
product: Windows
targetos: Windows
req.typenames: WS_REQUEST_SECURITY_TOKEN_ACTION
req.redist: 
---

# WS_REQUEST_SECURITY_TOKEN_ACTION enumeration


## -description


Defines which set of actions to use when negotiating security tokens using WS-Trust.
      


## -enum-fields




### -field WS_REQUEST_SECURITY_TOKEN_ACTION_ISSUE

Use the "request" action defined in WS-Trust.
        


### -field WS_REQUEST_SECURITY_TOKEN_ACTION_NEW_CONTEXT

Use the "request" action defined in WS-SecureConversation.
        


### -field WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT

Use the "renew" action defined in WS-SecureConversation. Requires <a href="https://msdn.microsoft.com/en-us/library/Dd323367(v=VS.85).aspx">WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN</a>.
        

