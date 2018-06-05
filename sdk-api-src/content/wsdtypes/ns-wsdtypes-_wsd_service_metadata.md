---
UID: NS:wsdtypes._WSD_SERVICE_METADATA
title: "_WSD_SERVICE_METADATA"
author: windows-sdk-content
description: Provides metadata regarding a service hosted by a device.
old-location: ncd\wsd_service_metadata_struct.htm
old-project: WsdApi
ms.assetid: 1f80e36f-06ca-41fc-bbd7-b44823c75d4d
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSD_SERVICE_METADATA, WSD_SERVICE_METADATA structure, _WSD_SERVICE_METADATA, ncd.wsd_service_metadata_struct, wsdtypes/WSD_SERVICE_METADATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SERVICE_METADATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_SERVICE_METADATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_SERVICE_METADATA structure


## -description


Provides metadata regarding a service hosted by a device.


## -struct-fields




### -field EndpointReference

Reference to a <a href="https://msdn.microsoft.com/fc9fed5c-8a5b-4960-836b-e083154b7d90">WSD_ENDPOINT_REFERENCE_LIST</a> structure that specifies the endpoints at which the service is available. 


### -field Types

Reference to a <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.


### -field ServiceId

The URI of the service. This URI must be valid when a <b>WSD_SERVICE_METADATA</b> structure is passed to <a href="https://msdn.microsoft.com/dc4cbed9-9ec4-4bbd-b1c9-89c4c11ff424">IWSDDeviceHost::SetMetadata</a>. Applications are responsible for URI validation.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

