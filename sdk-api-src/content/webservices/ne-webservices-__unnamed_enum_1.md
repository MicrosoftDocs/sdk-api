---
UID: NE:webservices.__unnamed_enum_1
title: "__unnamed_enum_1"
author: windows-sdk-content
description: A set of flags that control how mapped headers appear in an HTTP request or response.
old-location: wsw\ws_http_header_mapping_options.htm
tech.root: wsw
ms.assetid: cd11cae2-36af-4086-80f3-e99493bf9eb1
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WS_HTTP_HEADER_MAPPING_COMMA_SEPARATOR, WS_HTTP_HEADER_MAPPING_OPTIONS, WS_HTTP_HEADER_MAPPING_OPTIONS enumeration [Web Services for Windows], WS_HTTP_HEADER_MAPPING_QUOTED_VALUE, WS_HTTP_HEADER_MAPPING_SEMICOLON_SEPARATOR, __unnamed_enum_1, webservices/WS_HTTP_HEADER_MAPPING_COMMA_SEPARATOR, webservices/WS_HTTP_HEADER_MAPPING_OPTIONS, webservices/WS_HTTP_HEADER_MAPPING_QUOTED_VALUE, webservices/WS_HTTP_HEADER_MAPPING_SEMICOLON_SEPARATOR, wsw.ws_http_header_mapping_options
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
 - WS_HTTP_HEADER_MAPPING_OPTIONS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_1 enumeration


## -description


A set of flags that control how mapped headers appear in an HTTP request or response.
            


## -enum-fields




### -field WS_HTTP_HEADER_MAPPING_COMMA_SEPARATOR

If this flag is specified, repeating mapped headers are mapped
                    into a single HTTP header with each header value separated by a comma.
                


### -field WS_HTTP_HEADER_MAPPING_SEMICOLON_SEPARATOR

If this flag is specified, repeating mapped headers are mapped
                    into a single HTTP header with each header value separated by a semicolon.
                


### -field WS_HTTP_HEADER_MAPPING_QUOTED_VALUE

If this flag is specified, the mapped header value will be
                    quoted in the HTTP header.
                


## -remarks



If using repeating mapped headers, then either <b>WS_HTTP_HEADER_MAPPING_COMMA_SEPARATOR</b>or <b>WS_HTTP_HEADER_MAPPING_SEMICOLON_SEPARATOR</b> must be specified.
            

If using a header value which has a value containing characters that
                requires quotes in order to appear in an HTTP header, then 
                <b>WS_HTTP_HEADER_MAPPING_QUOTED_VALUE</b> must be specified.
            



