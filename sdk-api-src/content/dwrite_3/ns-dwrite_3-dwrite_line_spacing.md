---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

