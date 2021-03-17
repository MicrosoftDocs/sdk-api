---
UID: NS:wsdtypes._WSD_SERVICE_METADATA_LIST
title: WSD_SERVICE_METADATA_LIST (wsdtypes.h)
description: Represents a node in a single-linked list of service metadata structures.
helpviewer_keywords: ["WSD_SERVICE_METADATA_LIST","WSD_SERVICE_METADATA_LIST structure","ncd.wsd_service_metadata_list_struct","wsdtypes/WSD_SERVICE_METADATA_LIST"]
old-location: ncd\wsd_service_metadata_list_struct.htm
tech.root: ncd
ms.assetid: f5975443-00e3-44f0-9a69-02460d4312c5
ms.date: 12/05/2018
ms.keywords: WSD_SERVICE_METADATA_LIST, WSD_SERVICE_METADATA_LIST structure, ncd.wsd_service_metadata_list_struct, wsdtypes/WSD_SERVICE_METADATA_LIST
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
req.typenames: WSD_SERVICE_METADATA_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SERVICE_METADATA_LIST
 - wsdtypes/_WSD_SERVICE_METADATA_LIST
 - WSD_SERVICE_METADATA_LIST
 - wsdtypes/WSD_SERVICE_METADATA_LIST
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
 - WSD_SERVICE_METADATA_LIST
---

# WSD_SERVICE_METADATA_LIST structure


## -description

Represents a node in a single-linked list of service metadata structures.

## -struct-fields

### -field Next

Reference to the next node in the linked list of <b>WSD_SERVICE_METADATA_LIST</b> structures.

### -field Element

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_service_metadata">WSD_SERVICE_METADATA</a> structure that represents the service metadata referenced by this node.

## -see-also

<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_service_metadata">WSD_SERVICE_METADATA</a>