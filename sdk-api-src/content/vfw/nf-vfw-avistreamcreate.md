---
UID: NF:vfw.AVIStreamCreate
title: AVIStreamCreate function (vfw.h)
description: The AVIStreamCreate function creates a stream not associated with any file.
helpviewer_keywords: ["AVIStreamCreate","AVIStreamCreate function [Windows Multimedia]","_win32_AVIStreamCreate","multimedia.avistreamcreate","vfw/AVIStreamCreate"]
old-location: multimedia\avistreamcreate.htm
tech.root: Multimedia
ms.assetid: 8c784875-dc8f-4fd4-b267-0194cdbfa3c7
ms.date: 12/05/2018
ms.keywords: AVIStreamCreate, AVIStreamCreate function [Windows Multimedia], _win32_AVIStreamCreate, multimedia.avistreamcreate, vfw/AVIStreamCreate
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
 - AVIStreamCreate
 - vfw/AVIStreamCreate
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
 - AVIStreamCreate
---

# AVIStreamCreate function


## -description

The <b>AVIStreamCreate</b> function creates a stream not associated with any file.

## -parameters

### -param ppavi

Pointer to a buffer that receives the new stream interface.

### -param lParam1

Stream-handler specific information.

### -param lParam2

Stream-handler specific information.

### -param pclsidHandler

Pointer to the class identifier used for the stream.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

You should not need to call this function. Some functions, such as <a href="/windows/desktop/api/vfw/nf-vfw-createeditablestream">CreateEditableStream</a> and <a href="/windows/desktop/api/vfw/nf-vfw-avimakecompressedstream">AVIMakeCompressedStream</a>, use it internally.

The argument <i>ppavi</i> contains the address of a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>