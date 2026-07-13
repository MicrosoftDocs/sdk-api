---
UID: NS:webservices._WS_BYTE_ARRAY_DESCRIPTION
title: WS_BYTE_ARRAY_DESCRIPTION (webservices.h)
description: Specifies constraints on the set of values which can be deserialized. (WS_BYTE_ARRAY_DESCRIPTION)
helpviewer_keywords: ["WS_BYTE_ARRAY_DESCRIPTION","WS_BYTE_ARRAY_DESCRIPTION structure [Web Services for Windows]","webservices/WS_BYTE_ARRAY_DESCRIPTION","wsw.ws_byte_array_description"]
old-location: wsw\ws_byte_array_description.htm
tech.root: wsw
ms.assetid: 4bdc2956-387e-4cf6-93e1-3a3879c74ccf
ms.date: 12/05/2018
ms.keywords: WS_BYTE_ARRAY_DESCRIPTION, WS_BYTE_ARRAY_DESCRIPTION structure [Web Services for Windows], webservices/WS_BYTE_ARRAY_DESCRIPTION, wsw.ws_byte_array_description
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
req.typenames: WS_BYTE_ARRAY_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_BYTE_ARRAY_DESCRIPTION
 - webservices/_WS_BYTE_ARRAY_DESCRIPTION
 - WS_BYTE_ARRAY_DESCRIPTION
 - webservices/WS_BYTE_ARRAY_DESCRIPTION
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
 - WS_BYTE_ARRAY_DESCRIPTION
---

# WS_BYTE_ARRAY_DESCRIPTION structure


## -description

Specifies constraints on the set of values
                which can be deserialized.This type description is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_BYTE_ARRAY_TYPE</a> and is optional.

## -struct-fields

### -field minByteCount

Specifies the minimum number of bytes.

### -field maxByteCount

Specifies the maximum number of bytes.
