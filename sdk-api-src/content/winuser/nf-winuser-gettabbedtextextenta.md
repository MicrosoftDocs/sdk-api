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

# GetTabbedTextExtentA function


## -description


The <b>GetTabbedTextExtent</b> function computes the width and height of a character string. If the string contains one or more tab characters, the width of the string is based upon the specified tab stops. The <b>GetTabbedTextExtent</b> function uses the currently selected font to compute the dimensions of the string.


## -parameters




### -param hdc

TBD


### -param lpString [in]

A pointer to a character string.


### -param chCount

TBD


### -param nTabPositions [in]

The number of tab-stop positions in the array pointed to by the <i>lpnTabStopPositions</i> parameter.


### -param lpnTabStopPositions [in]

A pointer to an array containing the tab-stop positions, in device units. The tab stops must be sorted in increasing order; the smallest x-value should be the first item in the array.


#### - hDC [in]

A handle to the device context.


#### - nCount [in]

The length of the text string. For the ANSI function it is a BYTE count and for the Unicode function it is a WORD count. Note that for the ANSI function, characters in SBCS code pages take one byte each, while most characters in DBCS code pages take two bytes; for the Unicode function, most currently defined Unicode characters (those in the Basic Multilingual Plane (BMP)) are one WORD while Unicode surrogates are two WORDs.


## -returns



If the function succeeds, the return value is the dimensions of the string in logical units. The height is in the high-order word and the width is in the low-order word.

If the function fails, the return value is 0. <b>GetTabbedTextExtent</b> will fail if <i>hDC</i> is invalid and if <i>nTabPositions</i> is less than 0.




## -remarks



The current clipping region does not affect the width and height returned by the <b>GetTabbedTextExtent</b> function.

Because some devices do not place characters in regular cell arrays (that is, they kern the characters), the sum of the extents of the characters in a string may not be equal to the extent of the string.

If the <i>nTabPositions</i> parameter is zero and the <i>lpnTabStopPositions</i> parameter is <b>NULL</b>, tabs are expanded to eight times the average character width.

If <i>nTabPositions</i> is 1, the tab stops are separated by the distance specified by the first value in the array to which <i>lpnTabStopPositions</i> points.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/1cb78a75-752d-4e06-afdf-cd797f209114">TabbedTextOut</a>
 

 

