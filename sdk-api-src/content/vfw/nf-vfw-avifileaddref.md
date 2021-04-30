---
UID: NF:vfw.AVIFileAddRef
title: AVIFileAddRef function (vfw.h)
description: The AVIFileAddRef function increments the reference count of an AVI file.
helpviewer_keywords: ["AVIFileAddRef","AVIFileAddRef function [Windows Multimedia]","_win32_AVIFileAddRef","multimedia.avifileaddref","vfw/AVIFileAddRef"]
old-location: multimedia\avifileaddref.htm
tech.root: Multimedia
ms.assetid: f3dd4fa0-69e3-4249-8c74-7502d09ff341
ms.date: 12/05/2018
ms.keywords: AVIFileAddRef, AVIFileAddRef function [Windows Multimedia], _win32_AVIFileAddRef, multimedia.avifileaddref, vfw/AVIFileAddRef
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
 - AVIFileAddRef
 - vfw/AVIFileAddRef
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
 - AVIFileAddRef
---

# AVIFileAddRef function


## -description

The <b>AVIFileAddRef</b> function increments the reference count of an AVI file.

## -parameters

### -param pfile

Handle to an open AVI file.

## -returns

Returns the updated reference count for the file interface.

## -remarks

The argument <i>pfile</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>