---
UID: NF:vfw.AVIMakeFileFromStreams
title: AVIMakeFileFromStreams function (vfw.h)
description: The AVIMakeFileFromStreams function constructs an AVIFile interface pointer from separate streams.
helpviewer_keywords: ["AVIMakeFileFromStreams","AVIMakeFileFromStreams function [Windows Multimedia]","_win32_AVIMakeFileFromStreams","multimedia.avimakefilefromstreams","vfw/AVIMakeFileFromStreams"]
old-location: multimedia\avimakefilefromstreams.htm
tech.root: Multimedia
ms.assetid: 5c7a7564-188a-46b7-84ad-de2b1e3db621
ms.date: 12/05/2018
ms.keywords: AVIMakeFileFromStreams, AVIMakeFileFromStreams function [Windows Multimedia], _win32_AVIMakeFileFromStreams, multimedia.avimakefilefromstreams, vfw/AVIMakeFileFromStreams
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
 - AVIMakeFileFromStreams
 - vfw/AVIMakeFileFromStreams
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
 - AVIMakeFileFromStreams
---

# AVIMakeFileFromStreams function


## -description

The <b>AVIMakeFileFromStreams</b> function constructs an AVIFile interface pointer from separate streams.

## -parameters

### -param ppfile

Pointer to a buffer that receives the new file interface pointer.

### -param nStreams

Count of the number of streams in the array of stream interface pointers referenced by papStreams.

### -param papStreams

Pointer to an array of stream interface pointers.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

Use the <a href="/windows/desktop/api/vfw/nf-vfw-avifilerelease">AVIFileRelease</a> function to close the file.

Other functions can use the AVIFile interface created by this function to copy and edit the streams associated with the interface. For example, you can retrieve a specific stream by using <a href="/windows/desktop/api/vfw/nf-vfw-avifilegetstream">AVIFileGetStream</a> with the file interface pointer.

The argument <i>pfile</i> is the address of a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface. The argument <i>papStreams</i> is the address of a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/api/vfw/nf-vfw-avifilegetstream">AVIFileGetStream</a>



<a href="/windows/desktop/api/vfw/nf-vfw-avifilerelease">AVIFileRelease</a>