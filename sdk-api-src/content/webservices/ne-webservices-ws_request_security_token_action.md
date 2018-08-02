---
UID: NE:webservices.WS_REQUEST_SECURITY_TOKEN_ACTION
title: WS_REQUEST_SECURITY_TOKEN_ACTION
author: windows-sdk-content
description: Defines which set of actions to use when negotiating security tokens using WS-Trust.
old-location: wsw\ws_request_security_token_action.htm
old-project: wsw
ms.assetid: 1ef2ab60-c0a6-461a-9c93-fce74e8d76ba
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_REQUEST_SECURITY_TOKEN_ACTION, WS_REQUEST_SECURITY_TOKEN_ACTION enumeration [Web Services for Windows], WS_REQUEST_SECURITY_TOKEN_ACTION_ISSUE, WS_REQUEST_SECURITY_TOKEN_ACTION_NEW_CONTEXT, WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT, webservices/WS_REQUEST_SECURITY_TOKEN_ACTION, webservices/WS_REQUEST_SECURITY_TOKEN_ACTION_ISSUE, webservices/WS_REQUEST_SECURITY_TOKEN_ACTION_NEW_CONTEXT, webservices/WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT, wsw.ws_request_security_token_action
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
req.typenames: WS_REQUEST_SECURITY_TOKEN_ACTION
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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

Use the "renew" action defined in WS-SecureConversation. Requires <a href="https://msdn.microsoft.com/7a2063eb-ab60-43d5-bd8c-41ef132abf50">WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN</a>.
        

