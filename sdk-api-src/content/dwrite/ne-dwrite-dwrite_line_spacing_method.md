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

# DWRITE_LINE_SPACING_METHOD enumeration


## -description


The method used for line spacing in a text layout.


## -enum-fields




### -field DWRITE_LINE_SPACING_METHOD_DEFAULT

Line spacing depends solely on the content, adjusting to accommodate the size of fonts and inline objects.


### -field DWRITE_LINE_SPACING_METHOD_UNIFORM

Lines are explicitly set to uniform spacing, regardless of the size of fonts and inline objects. This can be useful to avoid the uneven appearance that can occur from font fallback.


### -field DWRITE_LINE_SPACING_METHOD_PROPORTIONAL

Line spacing and baseline distances are proportional to the computed values based on the content, the size of the fonts and inline objects.
          

<div class="alert"><b>Note</b>  This value is only available on Windows 10 or later and it can be used with <a href="https://msdn.microsoft.com/1bfca257-189c-4d18-628c-aff8217d2775">IDWriteTextLayout3::SetLineSpacing</a>, 
          but can not be used with <a href="https://msdn.microsoft.com/3629779a-5e50-43ea-b161-dd17598b5b43">IDWriteTextFormat::SetLineSpacing</a>.</div>
<div> </div>

## -remarks



The line spacing method is set by using the <a href="https://msdn.microsoft.com/3629779a-5e50-43ea-b161-dd17598b5b43">SetLineSpacing</a> method of the <a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a> or <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> interfaces.  To get  the current line spacing method of a text format or text layou use the <a href="https://msdn.microsoft.com/d9563d4d-0b7d-4921-b251-6ef1e24105f1">GetLineSpacing</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9563d4d-0b7d-4921-b251-6ef1e24105f1">GetLineSpacing</a>



<a href="https://msdn.microsoft.com/3629779a-5e50-43ea-b161-dd17598b5b43">SetLineSpacing</a>
 

 

