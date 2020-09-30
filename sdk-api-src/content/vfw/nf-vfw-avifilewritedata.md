---
UID: NF:vfw.AVIFileWriteData
title: AVIFileWriteData function (vfw.h)
description: The AVIFileWriteData function writes supplementary data (other than normal header, format, and stream data) to the file.
helpviewer_keywords: ["AVIFileWriteData","AVIFileWriteData function [Windows Multimedia]","_win32_AVIFileWriteData","multimedia.avifilewritedata","vfw/AVIFileWriteData"]
old-location: multimedia\avifilewritedata.htm
tech.root: Multimedia
ms.assetid: 27eef026-e401-44a2-9b46-a16b61026d2a
ms.date: 12/05/2018
ms.keywords: AVIFileWriteData, AVIFileWriteData function [Windows Multimedia], _win32_AVIFileWriteData, multimedia.avifilewritedata, vfw/AVIFileWriteData
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
 - AVIFileWriteData
 - vfw/AVIFileWriteData
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
 - AVIFileWriteData
---

# AVIFileWriteData function


## -description

The <b>AVIFileWriteData</b> function writes supplementary data (other than normal header, format, and stream data) to the file.

## -parameters

### -param pfile

Handle to an open AVI file.

### -param ckid

RIFF chunk identifier (four-character code) of the data.

### -param lpData

Pointer to the buffer used to write the data.

### -param cbData

Size, in bytes, of the memory block referenced by <i>lpData</i>.

## -returns

Returns zero if successful or an error otherwise. In an application has read-only access to the file, the error code AVIERR_READONLY is returned.

## -remarks

Use the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamwritedata">AVIStreamWriteData</a> function to write data that applies to an individual stream.

The argument <i>pfile</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>