---
UID: NE:webservices.__unnamed_enum_2
title: "__unnamed_enum_2"
author: windows-sdk-content
description: A set of flags that control how HTTP responses are mapped to the message object.
old-location: wsw\ws_http_response_mapping_options.htm
tech.root: wsw
ms.assetid: 9990496a-4410-4a40-8466-d32a8025c2e3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_HTTP_RESPONSE_MAPPING_OPTIONS, WS_HTTP_RESPONSE_MAPPING_OPTIONS enumeration [Web Services for Windows], WS_HTTP_RESPONSE_MAPPING_STATUS_CODE, WS_HTTP_RESPONSE_MAPPING_STATUS_TEXT, __unnamed_enum_2, webservices/WS_HTTP_RESPONSE_MAPPING_OPTIONS, webservices/WS_HTTP_RESPONSE_MAPPING_STATUS_CODE, webservices/WS_HTTP_RESPONSE_MAPPING_STATUS_TEXT, wsw.ws_http_response_mapping_options
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WS_HTTP_RESPONSE_MAPPING_OPTIONS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_2 enumeration


## -description


A set of flags that control how HTTP responses
                are mapped to the message object.
            


## -enum-fields




### -field WS_HTTP_RESPONSE_MAPPING_STATUS_CODE

If this flag is specified, the status code of the
                    HTTP response will be mapped to a message header named
                    "StatusCode".  The <a href="https://msdn.microsoft.com/abdff5ca-fb0d-4867-b729-5cfe18520f80">WsGetMappedHeader</a> function
                    can be used to retrieve the value from the message object.
                


### -field WS_HTTP_RESPONSE_MAPPING_STATUS_TEXT

If this flag is specified, the status text of the
                    HTTP response will be mapped to a message header named
                    "StatusText".  The <a href="https://msdn.microsoft.com/abdff5ca-fb0d-4867-b729-5cfe18520f80">WsGetMappedHeader</a> function
                    can be used to retrieve the value from the message object.
                

