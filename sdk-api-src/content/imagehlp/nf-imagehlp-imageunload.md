---
UID: NF:imagehlp.ImageUnload
title: ImageUnload function
author: windows-sdk-content
description: Deallocates resources from a previous call to the ImageLoad function.
old-location: base\imageunload.htm
tech.root: Debug
ms.assetid: 9cebd32f-11fe-4dfe-9579-b219d62c3e74
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ImageUnload, ImageUnload function, _win32_imageunload, base.imageunload, imagehlp/ImageUnload
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ImageUnload
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageUnload function


## -description


Deallocates resources from a previous call to the 
<a href="https://msdn.microsoft.com/e88e6417-a805-43c2-9f47-5180228cf175">ImageLoad</a> function.


## -parameters




### -param LoadedImage [in]

A pointer to a 
<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a> structure that is returned from a call to the 
<a href="https://msdn.microsoft.com/e88e6417-a805-43c2-9f47-5180228cf175">ImageLoad</a> function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


<a href="https://msdn.microsoft.com/e88e6417-a805-43c2-9f47-5180228cf175">ImageLoad</a> and 
<b>ImageUnload</b> share internal data that can be corrupted if multiple consecutive calls to 
<b>ImageLoad</b> are performed. Therefore, make sure that you have called 
<b>ImageLoad</b> only once before calling 
<b>ImageUnload</b>.




## -remarks



All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>



<a href="https://msdn.microsoft.com/e88e6417-a805-43c2-9f47-5180228cf175">ImageLoad</a>



<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a>
 

 

