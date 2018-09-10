---
UID: NF:wingdi.GetFontUnicodeRanges
title: GetFontUnicodeRanges function
author: windows-sdk-content
description: The GetFontUnicodeRanges function returns information about which Unicode characters are supported by a font. The information is returned as a GLYPHSET structure.
old-location: gdi\getfontunicoderanges.htm
tech.root: gdi
ms.assetid: 51b0ab12-c467-4a89-8173-fdc513868aae
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFontUnicodeRanges, GetFontUnicodeRanges function [Windows GDI], _win32_GetFontUnicodeRanges, gdi.getfontunicoderanges, wingdi/GetFontUnicodeRanges
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-L1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetFontUnicodeRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFontUnicodeRanges function


## -description


The <b>GetFontUnicodeRanges</b> function returns information about which Unicode characters are supported by a font. The information is returned as a <a href="https://msdn.microsoft.com/b8ac8d3f-b062-491c-966f-02f3d4c11419">GLYPHSET</a> structure.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpgs [out]

A pointer to a <a href="https://msdn.microsoft.com/b8ac8d3f-b062-491c-966f-02f3d4c11419">GLYPHSET</a> structure that receives the glyph set information. If this parameter is <b>NULL</b>, the function returns the size of the <b>GLYPHSET</b> structure required to store the information.


## -returns



If the function succeeds, it returns number of bytes written to the GLYPHSET structure or, if the <i>lpgs</i> parameter is <b>NULL</b>, it returns the size of the GLYPHSET structure required to store the information.

If the function fails, it returns zero. No extended error information is available.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b8ac8d3f-b062-491c-966f-02f3d4c11419">GLYPHSET</a>
 

 

