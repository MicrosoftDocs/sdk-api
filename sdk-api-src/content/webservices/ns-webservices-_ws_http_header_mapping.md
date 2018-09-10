---
UID: NS:webservices._WS_HTTP_HEADER_MAPPING
title: "_WS_HTTP_HEADER_MAPPING"
author: windows-sdk-content
description: Specifies an individual header that is mapped as part of WS_HTTP_MESSAGE_MAPPING.
old-location: wsw\ws_http_header_mapping.htm
tech.root: wsw
ms.assetid: bca1f244-4692-42bb-bbd7-c96647038a06
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_HTTP_HEADER_MAPPING, WS_HTTP_HEADER_MAPPING structure [Web Services for Windows], _WS_HTTP_HEADER_MAPPING, webservices/WS_HTTP_HEADER_MAPPING, wsw.ws_http_header_mapping
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - WS_HTTP_HEADER_MAPPING
product: Windows
targetos: Windows
req.typenames: WS_HTTP_HEADER_MAPPING
req.redist: 
---

# _WS_HTTP_HEADER_MAPPING structure


## -description


Specifies an individual header that is mapped as part of <a href="https://msdn.microsoft.com/dff8217e-769d-4f0b-acf2-02d6e43589cf">WS_HTTP_MESSAGE_MAPPING</a>.
            


## -struct-fields




### -field headerName

The name of the HTTP header.
                


### -field headerMappingOptions

A set of flags that control how headers are mapped.  
                    See <a href="https://msdn.microsoft.com/cd11cae2-36af-4086-80f3-e99493bf9eb1">WS_HTTP_HEADER_MAPPING_OPTIONS</a> for more information.
                

