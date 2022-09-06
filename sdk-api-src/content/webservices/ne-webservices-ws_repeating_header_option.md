---
UID: NE:webservices.__unnamed_enum_41
title: WS_REPEATING_HEADER_OPTION (webservices.h)
description: This enum is used to specify whether a header is expected to appear more than once in a message.
helpviewer_keywords: ["WS_REPEATING_HEADER","WS_REPEATING_HEADER_OPTION","WS_REPEATING_HEADER_OPTION enumeration [Web Services for Windows]","WS_SINGLETON_HEADER","webservices/WS_REPEATING_HEADER","webservices/WS_REPEATING_HEADER_OPTION","webservices/WS_SINGLETON_HEADER","wsw.ws_repeating_header_option"]
old-location: wsw\ws_repeating_header_option.htm
tech.root: wsw
ms.assetid: 7bbe5aba-e7b6-483d-8782-714a38ef4a99
ms.date: 12/05/2018
ms.keywords: WS_REPEATING_HEADER, WS_REPEATING_HEADER_OPTION, WS_REPEATING_HEADER_OPTION enumeration [Web Services for Windows], WS_SINGLETON_HEADER, webservices/WS_REPEATING_HEADER, webservices/WS_REPEATING_HEADER_OPTION, webservices/WS_SINGLETON_HEADER, wsw.ws_repeating_header_option
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_REPEATING_HEADER_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_REPEATING_HEADER_OPTION
 - webservices/WS_REPEATING_HEADER_OPTION
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
 - WS_REPEATING_HEADER_OPTION
---

# WS_REPEATING_HEADER_OPTION enumeration


## -description

This enum is used to specify whether a header is expected
                to appear more than once in a message.

## -enum-fields

### -field WS_REPEATING_HEADER:1

The header may appear more than once in the message.

### -field WS_SINGLETON_HEADER:2

The header may appear at most once in the message.
                    When this option is specified, the function 
                    ensures that the specified header appears
                    at most once in the message.

