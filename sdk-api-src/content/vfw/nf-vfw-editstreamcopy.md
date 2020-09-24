---
UID: NF:vfw.EditStreamCopy
title: EditStreamCopy function (vfw.h)
description: The EditStreamCopy function copies an editable stream (or a portion of it) into a temporary stream.
helpviewer_keywords: ["EditStreamCopy","EditStreamCopy function [Windows Multimedia]","_win32_EditStreamCopy","multimedia.editstreamcopy","vfw/EditStreamCopy"]
old-location: multimedia\editstreamcopy.htm
tech.root: Multimedia
ms.assetid: c1548359-42ed-4d13-b72d-e7269a7c3482
ms.date: 12/05/2018
ms.keywords: EditStreamCopy, EditStreamCopy function [Windows Multimedia], _win32_EditStreamCopy, multimedia.editstreamcopy, vfw/EditStreamCopy
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
 - EditStreamCopy
 - vfw/EditStreamCopy
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
 - EditStreamCopy
---

# EditStreamCopy function


## -description

The <b>EditStreamCopy</b> function copies an editable stream (or a portion of it) into a temporary stream.

## -parameters

### -param pavi

Handle to the stream being copied.

### -param plStart

Starting position within the stream being copied. The starting position is returned.

### -param plLength

Amount of data to copy from the stream referenced by <i>pavi</i>. The length of the copied data is returned.

### -param ppResult

Pointer to a buffer that receives the handle created for the new stream.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

The stream that is copied must be created by the <b>CreateEditableStream</b> function or one of the stream editing functions.

The temporary stream can be treated as any other AVI stream.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>