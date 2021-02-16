---
UID: NS:wsdtypes._WSD_RELATIONSHIP_METADATA
title: WSD_RELATIONSHIP_METADATA (wsdtypes.h)
description: Provides metadata about the relationship between two or more services.
helpviewer_keywords: ["WSD_RELATIONSHIP_METADATA","WSD_RELATIONSHIP_METADATA structure","ncd.wsd_relationship_metadata","wsdtypes/WSD_RELATIONSHIP_METADATA"]
old-location: ncd\wsd_relationship_metadata.htm
tech.root: ncd
ms.assetid: 232ea033-f368-4a37-9bec-ba5dc0d9b60f
ms.date: 12/05/2018
ms.keywords: WSD_RELATIONSHIP_METADATA, WSD_RELATIONSHIP_METADATA structure, ncd.wsd_relationship_metadata, wsdtypes/WSD_RELATIONSHIP_METADATA
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
req.typenames: WSD_RELATIONSHIP_METADATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_RELATIONSHIP_METADATA
 - wsdtypes/_WSD_RELATIONSHIP_METADATA
 - WSD_RELATIONSHIP_METADATA
 - wsdtypes/WSD_RELATIONSHIP_METADATA
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
 - WSD_RELATIONSHIP_METADATA
---

# WSD_RELATIONSHIP_METADATA structure


## -description

Provides metadata about the relationship between two or more services.

## -struct-fields

### -field Type

A WS-Discovery Type.

### -field Data

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_host_metadata">WSD_HOST_METADATA</a> structure that contains metadata for all services hosted by a device.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.