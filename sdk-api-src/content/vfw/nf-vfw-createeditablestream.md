---
UID: NF:vfw.CreateEditableStream
title: CreateEditableStream function
author: windows-sdk-content
description: The CreateEditableStream function creates an editable stream. Use this function before using other stream editing functions.
old-location: multimedia\createeditablestream.htm
old-project: Multimedia
ms.assetid: 9c7b0ebe-c113-49c9-a74f-61f47e7c18af
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CreateEditableStream, CreateEditableStream function [Windows Multimedia], _win32_CreateEditableStream, multimedia.createeditablestream, vfw/CreateEditableStream
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
 - CreateEditableStream
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
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




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

