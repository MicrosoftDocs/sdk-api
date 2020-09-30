---
UID: NS:webservices._WS_DISALLOWED_USER_AGENT_SUBSTRINGS
title: WS_DISALLOWED_USER_AGENT_SUBSTRINGS (webservices.h)
description: Specifies the list of blocked UserAgent sub-string's. This is used with the WS_LISTENER_PROPERTY_DISALLOWED_USER_AGENT listener property.
helpviewer_keywords: ["WS_DISALLOWED_USER_AGENT_SUBSTRINGS","WS_DISALLOWED_USER_AGENT_SUBSTRINGS structure [Web Services for Windows]","webservices/WS_DISALLOWED_USER_AGENT_SUBSTRINGS","wsw.ws_disallowed_user_agent_substrings"]
old-location: wsw\ws_disallowed_user_agent_substrings.htm
tech.root: wsw
ms.assetid: 3a37275b-11e6-484a-adc2-1e9503d1b309
ms.date: 12/05/2018
ms.keywords: WS_DISALLOWED_USER_AGENT_SUBSTRINGS, WS_DISALLOWED_USER_AGENT_SUBSTRINGS structure [Web Services for Windows], webservices/WS_DISALLOWED_USER_AGENT_SUBSTRINGS, wsw.ws_disallowed_user_agent_substrings
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
req.typenames: WS_DISALLOWED_USER_AGENT_SUBSTRINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_DISALLOWED_USER_AGENT_SUBSTRINGS
 - webservices/_WS_DISALLOWED_USER_AGENT_SUBSTRINGS
 - WS_DISALLOWED_USER_AGENT_SUBSTRINGS
 - webservices/WS_DISALLOWED_USER_AGENT_SUBSTRINGS
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
 - WS_DISALLOWED_USER_AGENT_SUBSTRINGS
---

# WS_DISALLOWED_USER_AGENT_SUBSTRINGS structure


## -description

Specifies the list of blocked UserAgent sub-string's. This is
                used with the <a href="/windows/desktop/api/webservices/ne-webservices-ws_listener_property_id">WS_LISTENER_PROPERTY_DISALLOWED_USER_AGENT</a> 
                listener property.

## -struct-fields

### -field subStringCount

The number of items in 'prefixes'.

### -field subStrings

An array of WS_STRING*. Each WS_STRING* would be searched as a sub-string in the UserAgent HTTP header value.