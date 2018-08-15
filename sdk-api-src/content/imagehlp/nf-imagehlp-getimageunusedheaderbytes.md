---
UID: NF:imagehlp.GetImageUnusedHeaderBytes
title: GetImageUnusedHeaderBytes function
author: windows-sdk-content
description: Retrieves the offset and size of the part of the PE header that is currently unused.
old-location: base\getimageunusedheaderbytes.htm
old-project: debug
ms.assetid: 4ad9c833-693b-4c19-b397-f97f166efadc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetImageUnusedHeaderBytes, GetImageUnusedHeaderBytes function, _win32_getimageunusedheaderbytes, base.getimageunusedheaderbytes, imagehlp/GetImageUnusedHeaderBytes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imagehlp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - GetImageUnusedHeaderBytes
product: Windows
targetos: Windows
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetImageUnusedHeaderBytes function


## -description


Retrieves the offset and size of the part of the PE header that is currently unused.


## -parameters




### -param LoadedImage [in]

A pointer to a 
<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a> structure that is returned from a call to 
<a href="https://msdn.microsoft.com/42d5ea46-4b89-4d93-b9a9-18c2855df193">MapAndLoad</a> or <a href="https://msdn.microsoft.com/e88e6417-a805-43c2-9f47-5180228cf175">ImageLoad</a>.


### -param SizeUnusedHeaderBytes [out]

A pointer to a variable to receive the size, in bytes, of the part of the image's header which is unused.


## -returns



If the function succeeds, the return value is the offset from the base address of the first unused header byte.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>



<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a>
 

 

