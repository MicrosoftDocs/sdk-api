---
UID: NF:vfw.AVIStreamLength
title: AVIStreamLength function
author: windows-driver-content
description: The AVIStreamLength function returns the length of the stream.
old-location: multimedia\avistreamlength.htm
old-project: Multimedia
ms.assetid: 5fc5dd31-9f2d-48c8-8d7e-76add4608473
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: AVIStreamLength, AVIStreamLength function [Windows Multimedia], _win32_AVIStreamLength, multimedia.avistreamlength, vfw/AVIStreamLength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Avifil32.dll
api_name:
-	AVIStreamLength
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIStreamLength function


## -description



The <b>AVIStreamLength</b> function returns the length of the stream.




## -parameters




### -param pavi

Handle to an open stream.


## -returns



Returns the stream's length, in samples, if successful or -1 otherwise.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

