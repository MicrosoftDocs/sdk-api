---
UID: NF:vfw.AVISaveW
title: AVISaveW function (vfw.h)
description: The AVISave function builds a file by combining data streams from other files or from memory.helpviewer_keywords: ["AVISave","AVISave function [Windows Multimedia]","AVISaveA","AVISaveW","_win32_AVISave","multimedia.avisave","vfw/AVISave","vfw/AVISaveA","vfw/AVISaveW"]
old-location: multimedia\avisave.htm
tech.root: Multimedia
ms.assetid: 44200871-541c-4d67-ba12-61af06da8788
ms.date: 12/05/2018
ms.keywords: AVISave, AVISave function [Windows Multimedia], AVISaveA, AVISaveW, _win32_AVISave, multimedia.avisave, vfw/AVISave, vfw/AVISaveA, vfw/AVISaveW
f1_keywords:
- vfw/AVISave
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
req.unicode-ansi: AVISaveW (Unicode) and AVISaveA (ANSI)
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
- AVISave
- AVISaveA
- AVISaveW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVISaveW function


## -description



The <b>AVISave</b> function builds a file by combining data streams from other files or from memory.




## -parameters




### -param szFile

Null-terminated string containing the name of the file to save.


### -param pclsidHandler

Pointer to the file handler used to write the file. The file is created by calling the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-avifileopen">AVIFileOpen</a> function using this handler. If a handler is not specified, a default is selected from the registry based on the file extension.


### -param lpfnCallback

Pointer to a callback function for the save operation.


### -param nStreams

Number of streams saved in the file.


### -param pfile

Pointer to an AVI stream. This parameter is paired with <i>lpOptions</i>. The parameter pair can be repeated as a variable number of arguments.


### -param lpOptions

Pointer to an application-defined <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structure containing the compression options for the stream referenced by <i>pavi</i>. This parameter is paired with pavi. The parameter pair can be repeated as a variable number of arguments.


### -param arg7


## -returns



Returns AVIERR_OK if successful or an error otherwise.




## -remarks



This function creates a file, copies stream data into the file, closes the file, and releases the resources used by the new file. The last two parameters of this function identify a stream to save in the file and define the compression options of that stream. When saving more than one stream in an AVI file, repeat these two stream-specific parameters for each stream in the file.

A callback function (referenced by using <i>lpfnCallback</i>) can display status information and let the user cancel the save operation. The callback function uses the following format:


```cpp

LONG PASCAL SaveCallback(int nPercent)  

```


The <i>nPercent</i> parameter specifies the percentage of the file saved.

The callback function should return AVIERR_OK if the operation should continue and AVIERR_USERABORT if the user wishes to abort the save operation.

The argument <i>pavi</i> is a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
 

 

