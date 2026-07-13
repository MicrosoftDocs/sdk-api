---
UID: NS:webservices._WS_BYTES_DESCRIPTION
title: WS_BYTES_DESCRIPTION (webservices.h)
description: Specifies constraints on the set of values which can be deserialized. (WS_BYTES_DESCRIPTION)
helpviewer_keywords: ["WS_BYTES_DESCRIPTION","WS_BYTES_DESCRIPTION structure [Web Services for Windows]","webservices/WS_BYTES_DESCRIPTION","wsw.ws_bytes_description"]
old-location: wsw\ws_bytes_description.htm
tech.root: wsw
ms.assetid: 0c5384f9-0f6c-4523-bacb-ec3dd7321648
ms.date: 12/05/2018
ms.keywords: WS_BYTES_DESCRIPTION, WS_BYTES_DESCRIPTION structure [Web Services for Windows], webservices/WS_BYTES_DESCRIPTION, wsw.ws_bytes_description
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
req.typenames: WS_BYTES_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_BYTES_DESCRIPTION
 - webservices/_WS_BYTES_DESCRIPTION
 - WS_BYTES_DESCRIPTION
 - webservices/WS_BYTES_DESCRIPTION
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
 - WS_BYTES_DESCRIPTION
---

# WS_BYTES_DESCRIPTION structure


## -description

Specifies constraints on the set of values
                which can be deserialized. This type description is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_BYTES_TYPE</a> and is optional.

## -struct-fields

### -field minByteCount

Specifies the minimum number of bytes.

### -field maxByteCount

Specifies the maximum number of bytes.
