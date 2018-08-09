---
UID: NF:imagehlp.MapAndLoad
title: MapAndLoad function
author: windows-sdk-content
description: Maps an image and preloads data from the mapped file.
old-location: base\mapandload.htm
old-project: debug
ms.assetid: 42d5ea46-4b89-4d93-b9a9-18c2855df193
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MapAndLoad, MapAndLoad function, _win32_mapandload, base.mapandload, imagehlp/MapAndLoad
ms.prod: windows
ms.technology: windows-sdk
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
 - MapAndLoad
product: Windows
targetos: Windows
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
req.product: GDI+ 1.1
---

# MapAndLoad function


## -description


Maps an image and preloads data from the mapped file.


## -parameters




### -param ImageName [in]

The file name of the image (executable file or DLL) that is loaded.


### -param DllPath [in]

The path used to locate the image if the name provided cannot be found. If this parameter is <b>NULL</b>, then the search path rules set using the 
<a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a> function apply.


### -param LoadedImage [out]

A pointer to a 
<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a> structure that receives information about the image after it is loaded.


### -param DotDll [in]

The default extension to be used if the image name does not contain a file name extension. If the value is <b>TRUE</b>, a .DLL extension is used. If the value is <b>FALSE</b>, then an .EXE extension is used.


### -param ReadOnly [in]

The access mode. If this value is <b>TRUE</b>, the file is mapped for read-access only. If the value is <b>FALSE</b>, the file is mapped for read and write access.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>MapAndLoad</b> function maps an image and preloads data from the mapped file. The corresponding function, 
<a href="https://msdn.microsoft.com/63a39d2b-a3a1-4c91-be93-f9a681756293">UnMapAndLoad</a>, must be used to deallocate all resources that are allocated by the 
<b>MapAndLoad</b> function.
			

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>



<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a>



<a href="https://msdn.microsoft.com/63a39d2b-a3a1-4c91-be93-f9a681756293">UnMapAndLoad</a>
 

 

