---
UID: NE:dwrite.DWRITE_LINE_SPACING_METHOD
title: DWRITE_LINE_SPACING_METHOD
author: windows-sdk-content
description: The method used for line spacing in a text layout.
old-location: directwrite\dwrite_line_spacing_method.htm
tech.root: DirectWrite
ms.assetid: b75e8fee-ed6c-455d-8733-e6972792572c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DWRITE_LINE_SPACING_METHOD, DWRITE_LINE_SPACING_METHOD enumeration [Direct Write], DWRITE_LINE_SPACING_METHOD_DEFAULT, DWRITE_LINE_SPACING_METHOD_PROPORTIONAL, DWRITE_LINE_SPACING_METHOD_UNIFORM, directwrite.dwrite_line_spacing_method, dwrite/DWRITE_LINE_SPACING_METHOD, dwrite/DWRITE_LINE_SPACING_METHOD_DEFAULT, dwrite/DWRITE_LINE_SPACING_METHOD_PROPORTIONAL, dwrite/DWRITE_LINE_SPACING_METHOD_UNIFORM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_LINE_SPACING_METHOD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

