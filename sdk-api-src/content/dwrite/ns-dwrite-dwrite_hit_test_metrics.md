---
UID: NS:dwrite.DWRITE_HIT_TEST_METRICS
title: DWRITE_HIT_TEST_METRICS (dwrite.h)
description: Describes the region obtained by a hit test.
helpviewer_keywords: ["DWRITE_HIT_TEST_METRICS","DWRITE_HIT_TEST_METRICS structure [Direct Write]","directwrite.dwrite_hit_test_metrics","dwrite/DWRITE_HIT_TEST_METRICS"]
old-location: directwrite\dwrite_hit_test_metrics.htm
tech.root: DirectWrite
ms.assetid: 00aaed92-7078-4823-95c5-855c063c744a
ms.date: 12/05/2018
ms.keywords: DWRITE_HIT_TEST_METRICS, DWRITE_HIT_TEST_METRICS structure [Direct Write], directwrite.dwrite_hit_test_metrics, dwrite/DWRITE_HIT_TEST_METRICS
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
 - DWRITE_HIT_TEST_METRICS
 - dwrite/DWRITE_HIT_TEST_METRICS
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
 - DWRITE_HIT_TEST_METRICS
---

# DWRITE_HIT_TEST_METRICS structure


## -description

Describes the region obtained by a hit test.

## -struct-fields

### -field textPosition

Type: <b>UINT32</b>

The first text position within the hit region.

### -field length

Type: <b>UINT32</b>

The number of text positions within the hit region.

### -field left

Type: <b>FLOAT</b>

The x-coordinate of the upper-left corner of the hit region.

### -field top

Type: <b>FLOAT</b>

The y-coordinate of the upper-left corner of the hit region.

### -field width

Type: <b>FLOAT</b>

The width of the hit region.

### -field height

Type: <b>FLOAT</b>

The height of the hit region.

### -field bidiLevel

Type: <b>UINT32</b>

The <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzebidi">BIDI level</a> of the text positions within the hit region.

### -field isText

Type: <b>BOOL</b>

true if the hit region contains text; otherwise, false.

### -field isTrimmed

Type: <b>BOOL</b>

true if the text range is trimmed; otherwise, false.

