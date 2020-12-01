---
UID: NF:vfw.AVIFileEndRecord
title: AVIFileEndRecord function (vfw.h)
description: The AVIFileEndRecord function marks the end of a record when writing an interleaved file that uses a 1:1 interleave factor of video to audio data. (Each frame of video is interspersed with an equivalent amount of audio data.).
helpviewer_keywords: ["AVIFileEndRecord","AVIFileEndRecord function [Windows Multimedia]","_win32_AVIFileEndRecord","multimedia.avifileendrecord","vfw/AVIFileEndRecord"]
old-location: multimedia\avifileendrecord.htm
tech.root: Multimedia
ms.assetid: 0f04c384-7702-43d4-9c7e-e9e74d6f2796
ms.date: 12/05/2018
ms.keywords: AVIFileEndRecord, AVIFileEndRecord function [Windows Multimedia], _win32_AVIFileEndRecord, multimedia.avifileendrecord, vfw/AVIFileEndRecord
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
 - AVIFileEndRecord
 - vfw/AVIFileEndRecord
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
 - AVIFileEndRecord
---

# AVIFileEndRecord function


## -description

The <b>AVIFileEndRecord</b> function marks the end of a record when writing an interleaved file that uses a 1:1 interleave factor of video to audio data. (Each frame of video is interspersed with an equivalent amount of audio data.)

## -parameters

### -param pfile

Handle to an open AVI file.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

The <a href="/windows/desktop/api/vfw/nf-vfw-avisavea">AVISave</a> function uses this function internally. In general, applications should not need to use this function.

The argument <i>pfile</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>