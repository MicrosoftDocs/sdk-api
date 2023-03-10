---
UID: NS:wsdtypes._WSD_SERVICE_METADATA
title: WSD_SERVICE_METADATA (wsdtypes.h)
description: Provides metadata regarding a service hosted by a device.
helpviewer_keywords: ["WSD_SERVICE_METADATA","WSD_SERVICE_METADATA structure","ncd.wsd_service_metadata_struct","wsdtypes/WSD_SERVICE_METADATA"]
old-location: ncd\wsd_service_metadata_struct.htm
tech.root: ncd
ms.assetid: 1f80e36f-06ca-41fc-bbd7-b44823c75d4d
ms.date: 12/05/2018
ms.keywords: WSD_SERVICE_METADATA, WSD_SERVICE_METADATA structure, ncd.wsd_service_metadata_struct, wsdtypes/WSD_SERVICE_METADATA
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WSD_SERVICE_METADATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SERVICE_METADATA
 - wsdtypes/_WSD_SERVICE_METADATA
 - WSD_SERVICE_METADATA
 - wsdtypes/WSD_SERVICE_METADATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_SERVICE_METADATA
---

# WSD_SERVICE_METADATA structure


## -description

Provides metadata regarding a service hosted by a device.

## -struct-fields

### -field EndpointReference

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference_list">WSD_ENDPOINT_REFERENCE_LIST</a> structure that specifies the endpoints at which the service is available.

### -field Types

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_name_list">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.

### -field ServiceId

The URI of the service. This URI must be valid when a <b>WSD_SERVICE_METADATA</b> structure is passed to <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-setmetadata">IWSDDeviceHost::SetMetadata</a>. Applications are responsible for URI validation.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.