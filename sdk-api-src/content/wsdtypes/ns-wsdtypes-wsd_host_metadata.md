---
UID: NS:wsdtypes._WSD_HOST_METADATA
title: WSD_HOST_METADATA (wsdtypes.h)
description: Provides metadata for all services hosted by a device.
helpviewer_keywords: ["WSD_HOST_METADATA","WSD_HOST_METADATA structure","ncd.wsd_host_metadata_struct","wsdtypes/WSD_HOST_METADATA"]
old-location: ncd\wsd_host_metadata_struct.htm
tech.root: ncd
ms.assetid: da774582-3b27-470d-9b6a-ac2b106a47b9
ms.date: 12/05/2018
ms.keywords: WSD_HOST_METADATA, WSD_HOST_METADATA structure, ncd.wsd_host_metadata_struct, wsdtypes/WSD_HOST_METADATA
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
req.typenames: WSD_HOST_METADATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_HOST_METADATA
 - wsdtypes/_WSD_HOST_METADATA
 - WSD_HOST_METADATA
 - wsdtypes/WSD_HOST_METADATA
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
 - WSD_HOST_METADATA
---

# WSD_HOST_METADATA structure


## -description

Provides metadata for all services hosted by a device.

## -struct-fields

### -field Host

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_service_metadata">WSD_SERVICE_METADATA</a> structure that describes the parent service or the device.

### -field Hosted

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_service_metadata_list">WSD_SERVICE_METADATA_LIST</a> structure that represents the singly linked list of services hosted by the parent service.