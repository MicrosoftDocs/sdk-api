---
UID: NF:imagehlp.BindImage
title: BindImage function
author: windows-sdk-content
description: Computes the virtual address of each imported function.
old-location: base\bindimage.htm
tech.root: Debug
ms.assetid: d586bf3a-c911-44a3-bf92-7de35009f742
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BindImage, BindImage function, _win32_bindimage, base.bindimage, imagehlp/BindImage
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
 - BindImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BindImage function


## -description


Computes the virtual address of each imported function.

This function has been superseded by the 
<a href="https://msdn.microsoft.com/97edbe29-94e5-4d3c-b640-c92b7f01a159">BindImageEx</a> function. Use 
<b>BindImageEx</b> to provide a status routine or flags to control the image binding.


## -parameters




### -param ImageName [in]

The name of the file to be bound. This value can be a file name, a partial path, or a full path.


### -param DllPath [in]

The root of the search path to use if the file specified by the <i>ImageName</i> parameter cannot be opened.


### -param SymbolPath [in]

The root of the path to search for the file's corresponding symbol file.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A call to 
<b>BindImage</b> is equivalent to the following call: <code>BindImageEx( 0, ImageName, DllPath, SymbolPath, NULL );</code>

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/97edbe29-94e5-4d3c-b640-c92b7f01a159">BindImageEx</a>



<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>
 

 

