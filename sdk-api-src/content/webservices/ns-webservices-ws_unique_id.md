---
UID: NS:webservices._WS_UNIQUE_ID
title: WS_UNIQUE_ID (webservices.h)
description: Represents a unique ID URI.
helpviewer_keywords: ["WS_UNIQUE_ID","WS_UNIQUE_ID structure [Web Services for Windows]","webservices/WS_UNIQUE_ID","wsw.ws_unique_id"]
old-location: wsw\ws_unique_id.htm
tech.root: wsw
ms.assetid: b9fd4497-153f-45f9-8f23-0771ffc47830
ms.date: 12/05/2018
ms.keywords: WS_UNIQUE_ID, WS_UNIQUE_ID structure [Web Services for Windows], webservices/WS_UNIQUE_ID, wsw.ws_unique_id
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
req.typenames: WS_UNIQUE_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_UNIQUE_ID
 - webservices/_WS_UNIQUE_ID
 - WS_UNIQUE_ID
 - webservices/WS_UNIQUE_ID
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
 - WS_UNIQUE_ID
---

# WS_UNIQUE_ID structure


## -description

Represents a unique ID URI.

## -struct-fields

### -field uri

A string representation of the URI.  If length is zero,
                    then the unique ID is a guid, and the value is stored
                    in the guid field.  Otherwise, the URI is a string
                    and the string value is stored in the uri field.

### -field guid

If the uri.length field is 0, then this field contains
                    the GUID representation of the unique ID.  Otherwise
                    the value of the field is not defined.

## -remarks

This structure represents a URI that is used as a unique ID.
                It has native support for GUID-based URI's, but can also
                accommodate other unique-id URI's as a string.

