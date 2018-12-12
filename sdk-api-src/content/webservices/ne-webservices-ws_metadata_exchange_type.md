---
UID: NE:webservices.__unnamed_enum_93
title: WS_METADATA_EXCHANGE_TYPE
author: windows-sdk-content
description: WS_METADATA_EXCHANGE_TYPE enumeration
old-location: wsw\ws_metadata_exchange_type.htm
tech.root: wsw
ms.assetid: 35e66c77-db26-4806-9b56-51539b23bb61
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_METADATA_EXCHANGE_TYPE, WS_METADATA_EXCHANGE_TYPE enumeration [Web Services for Windows], WS_METADATA_EXCHANGE_TYPE_HTTP_GET, WS_METADATA_EXCHANGE_TYPE_MEX, WS_METADATA_EXCHANGE_TYPE_NONE, webservices/WS_METADATA_EXCHANGE_TYPE, webservices/WS_METADATA_EXCHANGE_TYPE_HTTP_GET, webservices/WS_METADATA_EXCHANGE_TYPE_MEX, webservices/WS_METADATA_EXCHANGE_TYPE_NONE, wsw.ws_metadata_exchange_type
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
 - WS_METADATA_EXCHANGE_TYPE
product: Windows
targetos: Windows
req.typenames: WS_METADATA_EXCHANGE_TYPE
req.redist: 
---

# WS_METADATA_EXCHANGE_TYPE enumeration


## -description




## -enum-fields




### -field WS_METADATA_EXCHANGE_TYPE_NONE

Disables WS-MetadataExchange/HTTP GET servicing on the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a>.  
                    This is the default value of  <a href="https://msdn.microsoft.com/f6b33fe5-a9e9-4733-8b6c-4b01009d3277">WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE</a> property.
                


### -field WS_METADATA_EXCHANGE_TYPE_MEX

Enables servicing of WS-MetadataExchange 1.1 request servicing on the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a>.
                


### -field WS_METADATA_EXCHANGE_TYPE_HTTP_GET

Enables servicing of HTTP GET request servicing on the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a> for metadata 
                    retrieval.
                

