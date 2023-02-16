---
UID: NS:wsdtypes.RESPONSEBODY_GetMetadata
title: RESPONSEBODY_GetMetadata (wsdtypes.h)
description: Represents a WS-MetadataExchange GetMetadata response message.
helpviewer_keywords: ["RESPONSEBODY_GetMetadata","RESPONSEBODY_GetMetadata structure","ncd.responsebody_getmetadata_struct","wsdtypes/RESPONSEBODY_GetMetadata"]
old-location: ncd\responsebody_getmetadata_struct.htm
tech.root: ncd
ms.assetid: 445513a8-5785-4822-bb2e-ec9b7665ac7a
ms.date: 12/05/2018
ms.keywords: RESPONSEBODY_GetMetadata, RESPONSEBODY_GetMetadata structure, ncd.responsebody_getmetadata_struct, wsdtypes/RESPONSEBODY_GetMetadata
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
req.typenames: RESPONSEBODY_GetMetadata
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESPONSEBODY_GetMetadata
 - wsdtypes/RESPONSEBODY_GetMetadata
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
 - RESPONSEBODY_GetMetadata
---

# RESPONSEBODY_GetMetadata structure


## -description

Represents a WS-MetadataExchange GetMetadata response message.

## -struct-fields

### -field Metadata

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_metadata_section_list">WSD_METADATA_SECTION_LIST</a> structure that contains a node in a single-linked list of metadata sections.

