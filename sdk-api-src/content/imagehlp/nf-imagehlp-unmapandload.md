---
UID: NF:imagehlp.UnMapAndLoad
title: UnMapAndLoad function
author: windows-sdk-content
description: Deallocate all resources that are allocated by a previous call to the MapAndLoad function.
old-location: base\unmapandload.htm
old-project: debug
ms.assetid: 63a39d2b-a3a1-4c91-be93-f9a681756293
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: UnMapAndLoad, UnMapAndLoad function, _win32_unmapandload, base.unmapandload, imagehlp/UnMapAndLoad
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
 - UnMapAndLoad
product: Windows
targetos: Windows
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
req.product: GDI+ 1.1
---

# UnMapAndLoad function


## -description


Deallocate all resources that are allocated by a previous call to the 
<a href="https://msdn.microsoft.com/42d5ea46-4b89-4d93-b9a9-18c2855df193">MapAndLoad</a> function.


## -parameters




### -param LoadedImage [in]

A pointer to a 
<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a> structure. This structure is obtained through a call to the 
<a href="https://msdn.microsoft.com/42d5ea46-4b89-4d93-b9a9-18c2855df193">MapAndLoad</a> function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>UnMapAndLoad</b> function must be used to deallocate all resources that are allocated by a previous call to 
<a href="https://msdn.microsoft.com/42d5ea46-4b89-4d93-b9a9-18c2855df193">MapAndLoad</a>. This function also writes a new checksum value into the image before the file is closed. This ensures that if a file is changed, it can be successfully loaded by the system loader.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>



<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a>



<a href="https://msdn.microsoft.com/42d5ea46-4b89-4d93-b9a9-18c2855df193">MapAndLoad</a>
 

 

