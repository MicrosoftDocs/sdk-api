---
UID: NF:vfw.AVIStreamReadFormat
title: AVIStreamReadFormat function
author: windows-sdk-content
description: The AVIStreamReadFormat function reads the stream format data.
old-location: multimedia\avistreamreadformat.htm
tech.root: Multimedia
ms.assetid: 312b7d20-89b2-4102-acf6-f603610dadd6
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: AVIStreamReadFormat, AVIStreamReadFormat function [Windows Multimedia], _win32_AVIStreamReadFormat, multimedia.avistreamreadformat, vfw/AVIStreamReadFormat
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
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIStreamReadFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamReadFormat function


## -description


The <b>AVIStreamReadFormat</b> function reads the stream format data.
      


## -parameters




### -param pavi

Handle to an open stream.
          


### -param lPos

Position in the stream used to obtain the format data.
          


### -param lpFormat

Pointer to a buffer to contain the format data.
          


### -param lpcbFormat

Pointer to a location indicating the size of the memory block referenced by <i>lpFormat</i>. On return, the value is changed to indicate the amount of data read. If <i>lpFormat</i> is <b>NULL</b>, this parameter can be used to obtain the amount of memory needed to return the format.


## -returns



Returns zero if successful or an error otherwise.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -remarks



Standard video stream handlers provide format information in a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure. Standard audio stream handlers provide format information in a <a href="https://msdn.microsoft.com/c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c">PCMWAVEFORMAT</a> structure. Other data streams can use other structures that describe the stream data.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

