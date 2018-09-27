---
UID: NS:webservices._WS_SERVICE_METADATA_DOCUMENT
title: "_WS_SERVICE_METADATA_DOCUMENT"
author: windows-sdk-content
description: Specifies the individual documents that make up the service metadata.
old-location: wsw\ws_service_metadata_document.htm
tech.root: wsw
ms.assetid: d15fb735-9f82-4dd2-8586-f67999ab9727
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WS_SERVICE_METADATA_DOCUMENT, WS_SERVICE_METADATA_DOCUMENT structure [Web Services for Windows], _WS_SERVICE_METADATA_DOCUMENT, webservices/WS_SERVICE_METADATA_DOCUMENT, wsw.ws_service_metadata_document
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
 - WS_SERVICE_METADATA_DOCUMENT
product: Windows
targetos: Windows
req.typenames: WS_SERVICE_METADATA_DOCUMENT
req.redist: 
---

# _WS_SERVICE_METADATA_DOCUMENT structure


## -description


Specifies the individual documents that make up the service metadata.
            


## -struct-fields




### -field content

A <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a>* representing the specific  XML Schema, WSDL or a Policy document.
                    The service model expects this to be valid for the lifetime of the <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a>.
                


### -field name

The name of the document which will be suffixed to the URL path on which this document is serviced for HTTP GET support
                    for metadata retrieval. Note that this can be set to <b>NULL</b> if the application is only using Ws-MetadataExchange 1.1 for servicing
                    metadata request.
                

See <a href="https://msdn.microsoft.com/f6b33fe5-a9e9-4733-8b6c-4b01009d3277">WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE</a> service endpoint property to see how to enable HTTP GET support or
                    WS-MetadataExchange 1.1 for servicing metadata request.
                

