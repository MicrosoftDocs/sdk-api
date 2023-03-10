---
UID: NF:vfw.CreateEditableStream
title: CreateEditableStream function (vfw.h)
description: The CreateEditableStream function creates an editable stream. Use this function before using other stream editing functions.
helpviewer_keywords: ["CreateEditableStream","CreateEditableStream function [Windows Multimedia]","_win32_CreateEditableStream","multimedia.createeditablestream","vfw/CreateEditableStream"]
old-location: multimedia\createeditablestream.htm
tech.root: Multimedia
ms.assetid: 9c7b0ebe-c113-49c9-a74f-61f47e7c18af
ms.date: 12/05/2018
ms.keywords: CreateEditableStream, CreateEditableStream function [Windows Multimedia], _win32_CreateEditableStream, multimedia.createeditablestream, vfw/CreateEditableStream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateEditableStream
 - vfw/CreateEditableStream
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
 - CreateEditableStream
---

# CreateEditableStream function


## -description

The <b>CreateEditableStream</b> function creates an editable stream. Use this function before using other stream editing functions.

## -parameters

### -param ppsEditable

Pointer to a buffer that receives the new stream handle.

### -param psSource

Handle to the stream supplying data for the new stream. Specify <b>NULL</b> to create an empty editable string that you can copy and paste data into.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

The stream pointer returned in <i>ppsEditable</i> must be used as the source stream in the other stream editing functions.

Internally, this function creates tables to keep track of changes to a stream. The original stream is never changed by the stream editing functions. The stream pointer created by this function can be used in any AVIFile function that accepts stream pointers. You can use this function on the same stream multiple times. A copy of a stream is not affected by changes in another copy.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>