---
UID: NE:dwrite_3.DWRITE_FONT_LINE_GAP_USAGE
title: DWRITE_FONT_LINE_GAP_USAGE (dwrite_3.h)
description: Specify whether DWRITE_FONT_METRICS::lineGap value should be part of the line metrics.
helpviewer_keywords: ["DWRITE_FONT_LINE_GAP_USAGE","DWRITE_FONT_LINE_GAP_USAGE enumeration [Direct Write]","DWRITE_FONT_LINE_GAP_USAGE_DEFAULT","DWRITE_FONT_LINE_GAP_USAGE_DISABLED","DWRITE_FONT_LINE_GAP_USAGE_ENABLED","directwrite.dwrite_font_line_gap_usage","dwrite_3/DWRITE_FONT_LINE_GAP_USAGE","dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_DEFAULT","dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_DISABLED","dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_ENABLED"]
old-location: directwrite\dwrite_font_line_gap_usage.htm
tech.root: DirectWrite
ms.assetid: 43d38cca-429d-7ee5-e94c-fba542e19bb5
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_LINE_GAP_USAGE, DWRITE_FONT_LINE_GAP_USAGE enumeration [Direct Write], DWRITE_FONT_LINE_GAP_USAGE_DEFAULT, DWRITE_FONT_LINE_GAP_USAGE_DISABLED, DWRITE_FONT_LINE_GAP_USAGE_ENABLED, directwrite.dwrite_font_line_gap_usage, dwrite_3/DWRITE_FONT_LINE_GAP_USAGE, dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_DEFAULT, dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_DISABLED, dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_ENABLED
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - DWRITE_FONT_LINE_GAP_USAGE
 - dwrite_3/DWRITE_FONT_LINE_GAP_USAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_FONT_LINE_GAP_USAGE
---

# DWRITE_FONT_LINE_GAP_USAGE enumeration


## -description

Specify whether <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics">DWRITE_FONT_METRICS</a>::lineGap value should be part of the line metrics

## -enum-fields

### -field DWRITE_FONT_LINE_GAP_USAGE_DEFAULT

The usage of the font line gap depends on the method used for text layout.

### -field DWRITE_FONT_LINE_GAP_USAGE_DISABLED

The font line gap is excluded from line spacing.

### -field DWRITE_FONT_LINE_GAP_USAGE_ENABLED

The font line gap is included in line spacing.

