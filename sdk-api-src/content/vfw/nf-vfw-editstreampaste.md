---
UID: NF:vfw.EditStreamPaste
title: EditStreamPaste function (vfw.h)
description: The EditStreamPaste function copies a stream (or a portion of it) from one stream and pastes it within another stream at a specified location.
helpviewer_keywords: ["EditStreamPaste","EditStreamPaste function [Windows Multimedia]","_win32_EditStreamPaste","multimedia.editstreampaste","vfw/EditStreamPaste"]
old-location: multimedia\editstreampaste.htm
tech.root: Multimedia
ms.assetid: c3c77ec1-0aa4-47ab-afc1-ed69d6aca201
ms.date: 12/05/2018
ms.keywords: EditStreamPaste, EditStreamPaste function [Windows Multimedia], _win32_EditStreamPaste, multimedia.editstreampaste, vfw/EditStreamPaste
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
 - EditStreamPaste
 - vfw/EditStreamPaste
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
 - EditStreamPaste
---

# EditStreamPaste function


## -description

The <b>EditStreamPaste</b> function copies a stream (or a portion of it) from one stream and pastes it within another stream at a specified location.

## -parameters

### -param pavi

Handle to an editable stream that will receive the copied stream data.

### -param plPos

Starting position to paste the data within the destination stream (referenced by <i>pavi</i>).

### -param plLength

Pointer to a buffer that receives the amount of data pasted in the stream.

### -param pstream

Handle to a stream supplying the data to paste. This stream does not need to be an editable stream.

### -param lStart

Starting position of the data to copy within the source stream.

### -param lEnd

Amount of data to copy from the source stream. If <i>lLength</i> is -1, the entire stream referenced by <i>pstream</i> is pasted in the other stream.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

The stream referenced by <i>pavi</i> must have been created by the <b>CreateEditableStream</b> function or one of the stream editing functions.

This function inserts data into the specified stream as a continuous block of data. It opens the specified data stream at the insertion point, pastes the specified stream segment at the insertion point, and appends the stream segment that trails the insertion point to the end of pasted segment.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/positioning-in-streams">Positioning in Streams</a>