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

# GetTextMetricsA function


## -description


The <b>GetTextMetrics</b> function fills the specified buffer with the metrics for the currently selected font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lptm [out]

A pointer to the <a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a> structure that receives the text metrics.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



To determine whether a font is a TrueType font, first select it into a DC, then call <b>GetTextMetrics</b>, and then check for TMPF_TRUETYPE in TEXTMETRIC.tmPitchAndFamily. Note that <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a> returns an uninitialized DC, which has "System" (a bitmap font) as the default font; thus the need to select a font into the DC.


#### Examples

For an example, see "Displaying Keyboard Input" in <a href="_win32_Using_Keyboard_Input_cpp">Using Keyboard Input</a> or <a href="https://msdn.microsoft.com/d21613ef-1ba4-40bb-b922-afe287556441">Drawing Text from Different Fonts on the Same Line</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/d3ec0350-2eb8-4843-88bb-d72cece710e7">GetTextAlign</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/c4c8c8f5-3651-481b-a55f-da7f49d92f3a">GetTextFace</a>



<a href="https://msdn.microsoft.com/55fb5a28-b7da-40d8-8e64-4b42c23fa8b1">SetTextJustification</a>



<a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a>
 

 

