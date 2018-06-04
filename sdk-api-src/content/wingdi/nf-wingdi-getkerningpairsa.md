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

# GetKerningPairsA function


## -description


The <b>GetKerningPairs</b> function retrieves the character-kerning pairs for the currently selected font for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param nPairs

TBD


### -param lpKernPair

TBD




#### - lpkrnpair [out]

A pointer to an array of <a href="https://msdn.microsoft.com/af7bfcf7-467b-4ea9-87c5-3622303b1d8b">KERNINGPAIR</a> structures that receives the kerning pairs. The array must contain at least as many structures as specified by the <i>nNumPairs</i> parameter. If this parameter is <b>NULL</b>, the function returns the total number of kerning pairs for the font.


#### - nNumPairs [in]

The number of pairs in the <i>lpkrnpair</i> array. If the font has more than <i>nNumPairs</i> kerning pairs, the function returns an error.


## -returns



If the function succeeds, the return value is the number of kerning pairs returned.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/af7bfcf7-467b-4ea9-87c5-3622303b1d8b">KERNINGPAIR</a>
 

 

