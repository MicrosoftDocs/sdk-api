---
UID: NF:vfw.AVISaveVW
title: AVISaveVW function
author: windows-sdk-content
description: The AVISaveV function builds a file by combining data streams from other files or from memory.
old-location: multimedia\avisavev.htm
tech.root: Multimedia
ms.assetid: e3810588-1be7-4e66-9b25-78aaa24b96c7
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: AVISaveV, AVISaveV function [Windows Multimedia], AVISaveVA, AVISaveVW, _win32_AVISaveV, multimedia.avisavev, vfw/AVISaveV, vfw/AVISaveVA, vfw/AVISaveVW
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
req.unicode-ansi: AVISaveVW (Unicode) and AVISaveVA (ANSI)
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
 - AVISaveV
 - AVISaveVA
 - AVISaveVW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVISaveVW function


## -description



The <b>AVISaveV</b> function builds a file by combining data streams from other files or from memory.




## -parameters




### -param szFile

Null-terminated string containing the name of the file to save.


### -param pclsidHandler

Pointer to the file handler used to write the file. The file is created by calling the <a href="https://msdn.microsoft.com/a5d7b278-7c80-42a3-94a4-5c012ad9a9fd">AVIFileOpen</a> function using this handler. If a handler is not specified, a default is selected from the registry based on the file extension.


### -param lpfnCallback

Pointer to a callback function used to display status information and to let the user cancel the save operation.


### -param nStreams

Number of streams to save.


### -param ppavi

Pointer to an array of pointers to the <b>AVISTREAM</b> function structures. The array uses one pointer for each stream.


### -param plpOptions

Pointer to an array of pointers to <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structures. The array uses one pointer for each stream.


## -returns



Returns AVIERR_OK if successful or an error otherwise.




## -remarks



This function is equivalent to the <a href="https://msdn.microsoft.com/44200871-541c-4d67-ba12-61af06da8788">AVISave</a> function except the streams are passed in an array instead of as a variable number of arguments.

This function creates a file, copies stream data into the file, closes the file, and releases the resources used by the new file. The last two parameters of this function are arrays that identify the streams to save in the file and define the compression options of those streams.

An application must allocate memory for the <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structures and the array of pointers to these structures.

The argument <i>ppavi</i> contains the address of a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

