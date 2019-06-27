---
UID: NS:dwrite_2.DWRITE_TEXT_METRICS1
title: DWRITE_TEXT_METRICS1 (dwrite_2.h)
author: windows-sdk-content
description: Contains the metrics associated with text after layout.
old-location: directwrite\dwrite_text_metrics1.htm
tech.root: DirectWrite
ms.assetid: 1C374FD8-8BDC-4719-921F-2E14A919E7EF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DWRITE_TEXT_METRICS1, DWRITE_TEXT_METRICS1 structure [Direct Write], PDWRITE_TEXT_METRICS1, PDWRITE_TEXT_METRICS1 structure pointer [Direct Write], directwrite.dwrite_text_metrics1, dwrite_2/DWRITE_TEXT_METRICS1, dwrite_2/PDWRITE_TEXT_METRICS1
ms.topic: struct
f1_keywords: 
 - "dwrite_2/DWRITE_TEXT_METRICS1"
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - dwrite_2.h
api_name:
 - DWRITE_TEXT_METRICS1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DWRITE_TEXT_METRICS1 structure


## -description


Contains the metrics associated with text after layout.All coordinates are in device independent pixels (DIPs).
      

<b>DWRITE_TEXT_METRICS1</b> extends <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_text_metrics">DWRITE_TEXT_METRICS</a> 
        to include the height of the formatted text.
      


## -struct-fields




### -field heightIncludingTrailingWhitespace

The height of the formatted text taking into account the trailing whitespace at the end of each line. This is
            pertinent for vertical text.


### -field DWRITE_TEXT_METRICS

 



