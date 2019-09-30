---
UID: NF:vfw.AVIStreamEndStreaming
title: AVIStreamEndStreaming function (vfw.h)
author: windows-sdk-content
description: The AVIStreamEndStreaming function ends streaming.
old-location: multimedia\avistreamendstreaming.htm
tech.root: Multimedia
ms.assetid: 8555bc24-c017-4d02-854b-e64cf9e8ae1b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamEndStreaming, AVIStreamEndStreaming function [Windows Multimedia], _win32_AVIStreamEndStreaming, multimedia.avistreamendstreaming, vfw/AVIStreamEndStreaming
ms.topic: function
f1_keywords: 
 - "vfw/AVIStreamEndStreaming"
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
 - AVIStreamEndStreaming
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamEndStreaming function


## -description



The <b>AVIStreamEndStreaming</b> function ends streaming.




## -parameters




### -param pavi

Pointer to a stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



Many stream implementations ignore this function.

The argument <i>pavi</i> contains a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
 

 

