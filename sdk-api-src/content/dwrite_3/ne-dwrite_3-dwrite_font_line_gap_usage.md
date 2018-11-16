---
UID: NE:dwrite_3.DWRITE_FONT_LINE_GAP_USAGE
title: DWRITE_FONT_LINE_GAP_USAGE
author: windows-sdk-content
description: Specify whether DWRITE_FONT_METRICS::lineGap value should be part of the line metrics.
old-location: directwrite\dwrite_font_line_gap_usage.htm
tech.root: DirectWrite
ms.assetid: 43d38cca-429d-7ee5-e94c-fba542e19bb5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DWRITE_FONT_LINE_GAP_USAGE, DWRITE_FONT_LINE_GAP_USAGE enumeration [Direct Write], DWRITE_FONT_LINE_GAP_USAGE_DEFAULT, DWRITE_FONT_LINE_GAP_USAGE_DISABLED, DWRITE_FONT_LINE_GAP_USAGE_ENABLED, directwrite.dwrite_font_line_gap_usage, dwrite_3/DWRITE_FONT_LINE_GAP_USAGE, dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_DEFAULT, dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_DISABLED, dwrite_3/DWRITE_FONT_LINE_GAP_USAGE_ENABLED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dwrite_3.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_FONT_LINE_GAP_USAGE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWRITE_FONT_LINE_GAP_USAGE enumeration


## -description


Specify whether <a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRICS</a>::lineGap value should be part of the line metrics


## -enum-fields




### -field DWRITE_FONT_LINE_GAP_USAGE_DEFAULT

The usage of the font line gap depends on the method used for text layout.


### -field DWRITE_FONT_LINE_GAP_USAGE_DISABLED

The font line gap is excluded from line spacing.


### -field DWRITE_FONT_LINE_GAP_USAGE_ENABLED

The font line gap is included in line spacing.

