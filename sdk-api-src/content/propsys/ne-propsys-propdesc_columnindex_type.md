---
UID: NE:propsys.PROPDESC_COLUMNINDEX_TYPE
title: PROPDESC_COLUMNINDEX_TYPE (propsys.h)
description: Indicates whether or how a property can be indexed.
helpviewer_keywords: ["PDCIT_INMEMORY","PDCIT_NONE","PDCIT_ONDEMAND","PDCIT_ONDISK","PDCIT_ONDISKALL","PDCIT_ONDISKVECTOR","PROPDESC_COLUMNINDEX_TYPE","PROPDESC_COLUMNINDEX_TYPE enumeration [Windows Properties]","_shell_PROPDESC_COLUMNINDEX_TYPE","properties.PROPDESC_COLUMNINDEX_TYPE","propsys/PDCIT_INMEMORY","propsys/PDCIT_NONE","propsys/PDCIT_ONDEMAND","propsys/PDCIT_ONDISK","propsys/PDCIT_ONDISKALL","propsys/PDCIT_ONDISKVECTOR","propsys/PROPDESC_COLUMNINDEX_TYPE","shell.PROPDESC_COLUMNINDEX_TYPE"]
old-location: properties\PROPDESC_COLUMNINDEX_TYPE.htm
tech.root: properties
ms.assetid: 71ba7578-a902-47ee-883c-0947751d278c
ms.date: 12/05/2018
ms.keywords: PDCIT_INMEMORY, PDCIT_NONE, PDCIT_ONDEMAND, PDCIT_ONDISK, PDCIT_ONDISKALL, PDCIT_ONDISKVECTOR, PROPDESC_COLUMNINDEX_TYPE, PROPDESC_COLUMNINDEX_TYPE enumeration [Windows Properties], _shell_PROPDESC_COLUMNINDEX_TYPE, properties.PROPDESC_COLUMNINDEX_TYPE, propsys/PDCIT_INMEMORY, propsys/PDCIT_NONE, propsys/PDCIT_ONDEMAND, propsys/PDCIT_ONDISK, propsys/PDCIT_ONDISKALL, propsys/PDCIT_ONDISKVECTOR, propsys/PROPDESC_COLUMNINDEX_TYPE, shell.PROPDESC_COLUMNINDEX_TYPE
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROPDESC_COLUMNINDEX_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROPDESC_COLUMNINDEX_TYPE
 - propsys/PROPDESC_COLUMNINDEX_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propsys.h
api_name:
 - PROPDESC_COLUMNINDEX_TYPE
---

# PROPDESC_COLUMNINDEX_TYPE enumeration


## -description

Indicates whether or how a property can be indexed.

## -enum-fields

### -field PDCIT_NONE:0

Never generate any index on this property.

### -field PDCIT_ONDISK:1

Always build the individual value index, but build the vector index only on demand.

### -field PDCIT_INMEMORY:2

Obsolete.

### -field PDCIT_ONDEMAND:3

<b>Windows 7 and later</b>. Build the individual value index or vector index the first time the index is used in a query to filter, group, or sort. After being generated the first time, the index is maintained for future queries. Most property indexes should be built on demand, because building and maintaining indexes is expensive and they should be built only if they will be used.

### -field PDCIT_ONDISKALL:4

<b>Windows 7 and later</b>. Always build both the individual value index and the vector index.

### -field PDCIT_ONDISKVECTOR:5

<b>Windows 7 and later</b>. Always build the vector index, but build the value index only on demand.

## -remarks

Windows Search builds indexes for the values found in the property store to efficiently support filtering, sorting, and grouping over indexed properties. There are two kinds of indexes: an individual value index that indexes an item by single values, and a vector index that indexes all the vector values of a row as a single index entry.

