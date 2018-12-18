---
UID: NF:imagehlp.SetImageConfigInformation
title: SetImageConfigInformation function
author: windows-sdk-content
description: Locates and changes the load configuration data of an image.
old-location: base\setimageconfiginformation.htm
tech.root: debug
ms.assetid: 396af0c0-2fb1-418b-bc2b-9e9eb63174bc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetImageConfigInformation, SetImageConfigInformation function, _win32_setimageconfiginformation, base.setimageconfiginformation, imagehlp/SetImageConfigInformation
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
 - SetImageConfigInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetImageConfigInformation function


## -description


Locates and changes the load configuration data of an image.


## -parameters




### -param LoadedImage [in]

A pointer to a 
<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a> structure that is returned from a call to 
<a href="https://msdn.microsoft.com/42d5ea46-4b89-4d93-b9a9-18c2855df193">MapAndLoad</a> or <b>LoadImage</b>.
					


### -param ImageConfigInformation [in]

A pointer to an 
<a href="https://msdn.microsoft.com/ebd42f1a-a5aa-4179-a2d0-61c50469d5c0">IMAGE_LOAD_CONFIG_DIRECTORY64</a> structure.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SetImageConfigInformation</b> function locates and returns the load configuration data of an image.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/5d9b6705-7e65-4a60-912e-8ffcff9d7921">GetImageConfigInformation</a>



<a href="https://msdn.microsoft.com/ebd42f1a-a5aa-4179-a2d0-61c50469d5c0">IMAGE_LOAD_CONFIG_DIRECTORY64</a>



<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>



<a href="https://msdn.microsoft.com/8bfc6b47-23d6-45e1-a733-5b938d6312da">LOADED_IMAGE</a>
 

 

