---
UID: NF:imagehlp.ImageLoad
title: ImageLoad function
author: windows-sdk-content
description: Maintains a list of loaded DLLs.
old-location: base\imageload.htm
tech.root: debug
ms.assetid: e88e6417-a805-43c2-9f47-5180228cf175
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImageLoad, ImageLoad function, _win32_imageload, base.imageload, imagehlp/ImageLoad
ms.topic: function
req.header: imagehlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - ImageLoad
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageLoad function


## -description


Maintains a list of loaded DLLs.


## -parameters




### -param DllName [in]

The name of the image.


### -param DllPath [in]

The path used to locate the image if the name provided cannot be found. If <b>NULL</b> is used, then the search path rules set forth in the 
<a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a> function apply.


## -returns



If the function succeeds, the return value is a pointer to a 
<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a> structure.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>ImageLoad</b> function is used to maintain a list of loaded DLLs. If the image has already been loaded, the prior 
<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a> is returned. Otherwise, the new image is added to the list.

The 
<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a> structure must be deallocated by the 
<a href="https://msdn.microsoft.com/9cebd32f-11fe-4dfe-9579-b219d62c3e74">ImageUnload</a> function.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>



<a href="https://msdn.microsoft.com/9cebd32f-11fe-4dfe-9579-b219d62c3e74">ImageUnload</a>



<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a>
 

 

