---
UID: NF:vfw.AVIFileReadData
title: AVIFileReadData function (vfw.h)
description: The AVIFileReadData function reads optional header data that applies to the entire file, such as author or copyright information.
helpviewer_keywords: ["AVIFileReadData","AVIFileReadData function [Windows Multimedia]","_win32_AVIFileReadData","multimedia.avifilereaddata","vfw/AVIFileReadData"]
old-location: multimedia\avifilereaddata.htm
tech.root: Multimedia
ms.assetid: 9eef2ef4-316e-43e8-8011-14f1c0b46d50
ms.date: 12/05/2018
ms.keywords: AVIFileReadData, AVIFileReadData function [Windows Multimedia], _win32_AVIFileReadData, multimedia.avifilereaddata, vfw/AVIFileReadData
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
 - AVIFileReadData
 - vfw/AVIFileReadData
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
 - AVIFileReadData
---

# AVIFileReadData function


## -description

The <b>AVIFileReadData</b> function reads optional header data that applies to the entire file, such as author or copyright information.

## -parameters

### -param pfile

Handle to an open AVI file.

### -param ckid

RIFF chunk identifier (four-character code) of the data.

### -param lpData

Pointer to the buffer used to return the data read.

### -param lpcbData

Pointer to a location indicating the size of the memory block referenced by <i>lpData</i>. If the data is read successfully, the value is changed to indicate the amount of data read.

## -returns

Returns zero if successful or an error otherwise. The return value AVIERR_NODATA indicates that data with the requested chunk identifier does not exist.

## -remarks

The optional header information is custom and does not have a set format.

The argument <i>pfile</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>