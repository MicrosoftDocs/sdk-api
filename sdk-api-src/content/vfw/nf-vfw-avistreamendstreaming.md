---
UID: NF:vfw.AVIStreamEndStreaming
title: AVIStreamEndStreaming function
author: windows-sdk-content
description: The AVIStreamEndStreaming function ends streaming.
old-location: multimedia\avistreamendstreaming.htm
tech.root: Multimedia
ms.assetid: 8555bc24-c017-4d02-854b-e64cf9e8ae1b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: AVIStreamEndStreaming, AVIStreamEndStreaming function [Windows Multimedia], _win32_AVIStreamEndStreaming, multimedia.avistreamendstreaming, vfw/AVIStreamEndStreaming
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The argument <i>pavi</i> contains a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

