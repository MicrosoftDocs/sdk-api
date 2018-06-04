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
 

 

