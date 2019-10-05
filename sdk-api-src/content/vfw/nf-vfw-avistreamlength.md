---
UID: NF:vfw.AVIStreamLength
title: AVIStreamLength function (vfw.h)
author: windows-sdk-content
description: The AVIStreamLength function returns the length of the stream.
old-location: multimedia\avistreamlength.htm
tech.root: Multimedia
ms.assetid: 5fc5dd31-9f2d-48c8-8d7e-76add4608473
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamLength, AVIStreamLength function [Windows Multimedia], _win32_AVIStreamLength, multimedia.avistreamlength, vfw/AVIStreamLength
ms.topic: function
f1_keywords: 
 - "vfw/AVIStreamLength"
dev_langs:
 - c++
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
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
api_name:
 - AVIStreamLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamLength function


## -description



The <b>AVIStreamLength</b> function returns the length of the stream.




## -parameters




### -param pavi

Handle to an open stream.


## -returns



Returns the stream's length, in samples, if successful or -1 otherwise.

The argument <i>pavi</i> is a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
 

 

