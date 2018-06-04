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

# RemoveFontMemResourceEx function


## -description


The <b>RemoveFontMemResourceEx</b> function removes the fonts added from a memory image file.


## -parameters




### -param h

TBD




#### - fh [in]

A handle to the font-resource. This handle is returned by the <a href="https://msdn.microsoft.com/ad5153ba-fa9d-4a07-9be3-a07b524c1539">AddFontMemResourceEx</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. No extended error information is available.




## -remarks



This function removes a font that was added by the <a href="https://msdn.microsoft.com/ad5153ba-fa9d-4a07-9be3-a07b524c1539">AddFontMemResourceEx</a> function. To remove the font, specify the same path and flags as were used in <b>AddFontMemResourceEx</b>. This function will only remove the font that is specified by <i>fh</i>.




## -see-also




<a href="https://msdn.microsoft.com/ad5153ba-fa9d-4a07-9be3-a07b524c1539">AddFontMemResourceEx</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>
 

 

