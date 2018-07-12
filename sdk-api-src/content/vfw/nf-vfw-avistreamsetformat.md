---
UID: NF:vfw.AVIStreamSetFormat
title: AVIStreamSetFormat function
author: windows-sdk-content
description: The AVIStreamSetFormat function sets the format of a stream at the specified position.
old-location: multimedia\avistreamsetformat.htm
old-project: Multimedia
ms.assetid: b896f674-823d-49c9-8e48-c5081e37a13a
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: AVIStreamSetFormat, AVIStreamSetFormat function [Windows Multimedia], _win32_AVIStreamSetFormat, multimedia.avistreamsetformat, vfw/AVIStreamSetFormat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
api_name:
 - AVIStreamSetFormat
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIStreamSetFormat function


## -description



The <b>AVIStreamSetFormat</b> function sets the format of a stream at the specified position.




## -parameters




### -param pavi

Handle to an open stream.


### -param lPos

Position in the stream to receive the format.


### -param lpFormat

Pointer to a structure containing the new format.


### -param cbFormat

Size, in bytes, of the block of memory referenced by <i>lpFormat</i>.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The handler for writing AVI files does not accept format changes. Besides setting the initial format for a stream, only changes in the palette of a video stream are allowed in an AVI file. The palette change must occur after any frames already written to the AVI file. Other handlers might impose different restrictions.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

