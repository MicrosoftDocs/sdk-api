---
UID: NS:dwrite_3.DWRITE_LINE_SPACING
title: DWRITE_LINE_SPACING
author: windows-sdk-content
description: "."
old-location: directwrite\dwrite_line_spacing.htm
old-project: DirectWrite
ms.assetid: bb589a7a-374f-52fc-2fa4-4cc72c6ce6dc
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: DWRITE_LINE_SPACING, DWRITE_LINE_SPACING structure [Direct Write], directwrite.dwrite_line_spacing, dwrite_3/DWRITE_LINE_SPACING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dwrite_3.h
api_name:
-	DWRITE_LINE_SPACING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_LINE_SPACING structure


## -description





## -struct-fields




### -field method

Type: <b><a href="https://msdn.microsoft.com/b75e8fee-ed6c-455d-8733-e6972792572c">DWRITE_LINE_SPACING_METHOD</a></b>

Method used to determine line spacing.


### -field height

Type: <b>FLOAT</b>

Spacing between lines. The interpretation of this parameter depends upon the line spacing method, as follows:
       

<ul>
<li>Line spacing: ignored</li>
<li>uniform line spacing: explicit distance in DIPs between lines</li>
<li>proportional line spacing: a scaling factor to be applied to the computed line height; 
       for each line, the height of the line is computed as for default line spacing, and the scaling factor is applied to that value.</li>
</ul>

### -field baseline

Type: <b>FLOAT</b>

Distance from top of line to baseline. 
       The interpretation of this parameter depends upon the line spacing method, as follows:
       

<ul>
<li>default line spacing: ignored</li>
<li>uniform line spacing: explicit distance in DIPs from the top of the line to the baseline</li>
<li>proportional line spacing: a scaling factor applied to the computed baseline; for each line, 
       the baseline distance is computed as for default line spacing, and the scaling factor is applied to that value.</li>
</ul>

### -field leadingBefore

Type: <b>FLOAT</b>

Proportion of the entire leading distributed before the line. The allowed value is between 0 and 1.0. The remaining
     leading is distributed after the line. It is ignored for the default and uniform line spacing methods.
     The leading that is available to distribute before or after the line depends on the values of the height and
     baseline parameters.


### -field fontLineGapUsage

Type: <b><a href="https://msdn.microsoft.com/43d38cca-429d-7ee5-e94c-fba542e19bb5">DWRITE_FONT_LINE_GAP_USAGE</a></b>

Specify whether <a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRICS</a>::lineGap value should be part of the line metrics.

