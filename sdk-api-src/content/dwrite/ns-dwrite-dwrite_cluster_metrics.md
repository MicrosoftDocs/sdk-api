---
UID: NS:dwrite.DWRITE_CLUSTER_METRICS
title: DWRITE_CLUSTER_METRICS (dwrite.h)
description: Contains information about a glyph cluster.
helpviewer_keywords: ["DWRITE_CLUSTER_METRICS","DWRITE_CLUSTER_METRICS structure [Direct Write]","directwrite.dwrite_cluster_metrics","dwrite/DWRITE_CLUSTER_METRICS"]
old-location: directwrite\dwrite_cluster_metrics.htm
tech.root: DirectWrite
ms.assetid: 738b7f15-fcc5-4960-ac1f-ca530c448271
ms.date: 12/05/2018
ms.keywords: DWRITE_CLUSTER_METRICS, DWRITE_CLUSTER_METRICS structure [Direct Write], directwrite.dwrite_cluster_metrics, dwrite/DWRITE_CLUSTER_METRICS
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_CLUSTER_METRICS
 - dwrite/DWRITE_CLUSTER_METRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_CLUSTER_METRICS
---

# DWRITE_CLUSTER_METRICS structure


## -description

Contains information about a glyph cluster.

## -struct-fields

### -field width

Type: <b>FLOAT</b>

The total advance width of all glyphs in the cluster.

### -field length

Type: <b>UINT16</b>

The number of text positions in the cluster.

### -field canWrapLineAfter

Type: <b>UINT16</b>

Indicates whether a line can be broken right after the cluster.

### -field isWhitespace

Type: <b>UINT16</b>

Indicates whether the cluster corresponds to a whitespace character.

### -field isNewline

Type: <b>UINT16</b>

Indicates whether the cluster corresponds to a newline character.

### -field isSoftHyphen

Type: <b>UINT16</b>

Indicates whether the cluster corresponds to a soft hyphen character.

### -field isRightToLeft

Type: <b>UINT16</b>

Indicates whether the cluster is read from right to left.

### -field padding

Type: <b>UINT16</b>

Reserved for future use.

