---
UID: NS:wsdtypes._WSD_METADATA_SECTION_LIST
title: WSD_METADATA_SECTION_LIST (wsdtypes.h)
description: Represents a node in a single-linked list of metadata sections.
helpviewer_keywords: ["WSD_METADATA_SECTION_LIST","WSD_METADATA_SECTION_LIST structure","ncd.wsd_metadata_section_list_struct","wsdtypes/WSD_METADATA_SECTION_LIST"]
old-location: ncd\wsd_metadata_section_list_struct.htm
tech.root: ncd
ms.assetid: e5c6373a-f365-499d-a971-472ffa557a41
ms.date: 12/05/2018
ms.keywords: WSD_METADATA_SECTION_LIST, WSD_METADATA_SECTION_LIST structure, ncd.wsd_metadata_section_list_struct, wsdtypes/WSD_METADATA_SECTION_LIST
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
req.typenames: WSD_METADATA_SECTION_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_METADATA_SECTION_LIST
 - wsdtypes/_WSD_METADATA_SECTION_LIST
 - WSD_METADATA_SECTION_LIST
 - wsdtypes/WSD_METADATA_SECTION_LIST
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
 - WSD_METADATA_SECTION_LIST
---

# WSD_METADATA_SECTION_LIST structure


## -description

Represents a node in a single-linked list of metadata sections.

## -struct-fields

### -field Next

Reference to the next node in the linked list of <b>WSD_METADATA_SECTION_LIST</b> structures.

### -field Element

The metadata section referenced by this node.

