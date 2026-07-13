---
UID: NF:vfw.AVISaveVA
title: AVISaveVA function (vfw.h)
description: The AVISaveV function builds a file by combining data streams from other files or from memory. (ANSI)
helpviewer_keywords: ["AVISaveVA", "vfw/AVISaveVA"]
old-location: multimedia\avisavev.htm
tech.root: Multimedia
ms.assetid: e3810588-1be7-4e66-9b25-78aaa24b96c7
ms.date: 12/05/2018
ms.keywords: AVISaveV, AVISaveV function [Windows Multimedia], AVISaveVA, AVISaveVW, _win32_AVISaveV, multimedia.avisavev, vfw/AVISaveV, vfw/AVISaveVA, vfw/AVISaveVW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVISaveVA
 - vfw/AVISaveVA
dev_langs:
 - c++
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
---

# AVISaveVA function


## -description

The <b>AVISaveV</b> function builds a file by combining data streams from other files or from memory.

## -parameters

### -param szFile

Null-terminated string containing the name of the file to save.

### -param pclsidHandler

Pointer to the file handler used to write the file. The file is created by calling the <a href="/windows/desktop/api/vfw/nf-vfw-avifileopen">AVIFileOpen</a> function using this handler. If a handler is not specified, a default is selected from the registry based on the file extension.

### -param lpfnCallback

Pointer to a callback function used to display status information and to let the user cancel the save operation.

### -param nStreams

Number of streams to save.

### -param ppavi

Pointer to an array of pointers to the <b>AVISTREAM</b> function structures. The array uses one pointer for each stream.

### -param plpOptions

Pointer to an array of pointers to <a href="/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structures. The array uses one pointer for each stream.

## -returns

Returns AVIERR_OK if successful or an error otherwise.

## -remarks

This function is equivalent to the <a href="/windows/desktop/api/vfw/nf-vfw-avisavea">AVISave</a> function except the streams are passed in an array instead of as a variable number of arguments.

This function creates a file, copies stream data into the file, closes the file, and releases the resources used by the new file. The last two parameters of this function are arrays that identify the streams to save in the file and define the compression options of those streams.

An application must allocate memory for the <a href="/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structures and the array of pointers to these structures.

The argument <i>ppavi</i> contains the address of a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.





> [!NOTE]
> The vfw.h header defines AVISaveV as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
