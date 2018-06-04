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
 

 

