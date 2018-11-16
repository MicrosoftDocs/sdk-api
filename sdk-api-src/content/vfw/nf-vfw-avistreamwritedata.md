---
UID: NF:vfw.AVIStreamWriteData
title: AVIStreamWriteData function
author: windows-sdk-content
description: The AVIStreamWriteData function writes optional header information to the stream.
old-location: multimedia\avistreamwritedata.htm
tech.root: Multimedia
ms.assetid: 2ca91df6-4721-4282-8b88-81e76d2ab94f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AVIStreamWriteData, AVIStreamWriteData function [Windows Multimedia], _win32_AVIStreamWriteData, multimedia.avistreamwritedata, vfw/AVIStreamWriteData
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
 - AVIStreamWriteData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- AVIStreamWriteData
: 
---

# AVIStreamWriteData function


## -description



The <b>AVIStreamWriteData</b> function writes optional header information to the stream.




## -parameters




### -param pavi

Handle to an open stream.


### -param fcc

Four-character code identifying the data.


### -param lp

Pointer to a buffer containing the data to write.


### -param cb

Number of bytes of data to write into the stream.


## -returns



Returns zero if successful or an error otherwise. The return value AVIERR_READONLY indicates the file was opened without write access.




## -remarks



Use the <a href="https://msdn.microsoft.com/9a306939-7b4f-4e0b-8340-270725da74c3">AVIStreamWrite</a> function to write the multimedia content of the stream. Use <a href="https://msdn.microsoft.com/27eef026-e401-44a2-9b46-a16b61026d2a">AVIFileWriteData</a> to write data that applies to an entire file.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

