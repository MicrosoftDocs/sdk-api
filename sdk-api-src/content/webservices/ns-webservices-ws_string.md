---
UID: NS:webservices._WS_STRING
title: WS_STRING (webservices.h)
description: An array of Unicode characters and a length.
helpviewer_keywords: ["WS_STRING","WS_STRING structure [Web Services for Windows]","webservices/WS_STRING","wsw.ws_string"]
old-location: wsw\ws_string.htm
tech.root: wsw
ms.assetid: eb6c7397-6b15-4e79-89ec-585861113edf
ms.date: 12/05/2018
ms.keywords: WS_STRING, WS_STRING structure [Web Services for Windows], webservices/WS_STRING, wsw.ws_string
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
req.typenames: WS_STRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_STRING
 - webservices/_WS_STRING
 - WS_STRING
 - webservices/WS_STRING
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
 - WS_STRING
---

# WS_STRING structure


## -description

An array of Unicode characters and a length.

## -struct-fields

### -field length

The number of characters in the string.

### -field chars

The array of characters that make up the string.

## -remarks

The string is not required to be zero terminated.  If it is
                zero terminated, then the terminating character is not included
                in the length.
            

The macro <a href="/windows/desktop/api/webservices/nf-webservices-ws_string_value">WS_STRING_VALUE</a> can be used to initialize
                this structure if the string is a constant string.