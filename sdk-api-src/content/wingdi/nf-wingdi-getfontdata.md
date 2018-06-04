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

# GetFontData function


## -description


The <b>GetFontData</b> function retrieves font metric data for a TrueType font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param dwTable [in]

The name of a font metric table from which the font data is to be retrieved. This parameter can identify one of the metric tables documented in the TrueType Font Files specification published by Microsoft Corporation. If this parameter is zero, the information is retrieved starting at the beginning of the file for TrueType font files or from the beginning of the data for the currently selected font for TrueType Collection files. To retrieve the data from the beginning of the file for TrueType Collection files specify 'ttcf' (0x66637474).


### -param dwOffset [in]

The offset from the beginning of the font metric table to the location where the function should begin retrieving information. If this parameter is zero, the information is retrieved starting at the beginning of the table specified by the <i>dwTable</i> parameter. If this value is greater than or equal to the size of the table, an error occurs.


### -param pvBuffer

TBD


### -param cjBuffer

TBD




#### - cbData [in]

The length, in bytes, of the information to be retrieved. If this parameter is zero, <b>GetFontData</b> returns the size of the data specified in the <i>dwTable</i> parameter.


#### - lpvBuffer [out]

A pointer to a buffer that receives the font information. If this parameter is <b>NULL</b>, the function returns the size of the buffer required for the font data.


## -returns



If the function succeeds, the return value is the number of bytes returned.

If the function fails, the return value is GDI_ERROR.




## -remarks



This function is intended to be used to retrieve TrueType font information directly from the font file by font-manipulation applications. For information about embedding fonts see the <a href="https://msdn.microsoft.com/1ba019c7-9ba6-429d-bbdc-7e182d93ab75">Font Embedding Reference</a>.

An application can sometimes use the <b>GetFontData</b> function to save a TrueType font with a document. To do this, the application determines whether the font can be embedded by checking the <b>otmfsType</b> member of the <a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a> structure. If bit 1 of <b>otmfsType</b> is set, embedding is not permitted for the font. If bit 1 is clear, the font can be embedded. If bit 2 is set, the embedding is read-only. If embedding is permitted, the application can retrieve the entire font file, specifying zero for the <i>dwTable</i>, <i>dwOffset</i>, and <i>cbData</i> parameters.

If an application attempts to use this function to retrieve information for a non-TrueType font, an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a>



<a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a>
 

 

