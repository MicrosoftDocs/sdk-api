---
UID: NS:webservices._WS_HTTP_HEADER_MAPPING
title: WS_HTTP_HEADER_MAPPING (webservices.h)
description: Specifies an individual header that is mapped as part of WS_HTTP_MESSAGE_MAPPING.
helpviewer_keywords: ["WS_HTTP_HEADER_MAPPING","WS_HTTP_HEADER_MAPPING structure [Web Services for Windows]","webservices/WS_HTTP_HEADER_MAPPING","wsw.ws_http_header_mapping"]
old-location: wsw\ws_http_header_mapping.htm
tech.root: wsw
ms.assetid: bca1f244-4692-42bb-bbd7-c96647038a06
ms.date: 12/05/2018
ms.keywords: WS_HTTP_HEADER_MAPPING, WS_HTTP_HEADER_MAPPING structure [Web Services for Windows], webservices/WS_HTTP_HEADER_MAPPING, wsw.ws_http_header_mapping
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
req.typenames: WS_HTTP_HEADER_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_HTTP_HEADER_MAPPING
 - webservices/_WS_HTTP_HEADER_MAPPING
 - WS_HTTP_HEADER_MAPPING
 - webservices/WS_HTTP_HEADER_MAPPING
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
 - WS_HTTP_HEADER_MAPPING
---

# WS_HTTP_HEADER_MAPPING structure


## -description

Specifies an individual header that is mapped as part of <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_message_mapping">WS_HTTP_MESSAGE_MAPPING</a>.

## -struct-fields

### -field headerName

The name of the HTTP header.

### -field headerMappingOptions

A set of flags that control how headers are mapped.  
                    See <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_canonicalization_algorithm">WS_HTTP_HEADER_MAPPING_OPTIONS</a> for more information.