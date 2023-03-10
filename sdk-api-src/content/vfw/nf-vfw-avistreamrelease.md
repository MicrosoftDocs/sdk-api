---
UID: NF:vfw.AVIStreamRelease
title: AVIStreamRelease function (vfw.h)
description: The AVIStreamRelease function decrements the reference count of an AVI stream interface handle, and closes the stream if the count reaches zero.
helpviewer_keywords: ["AVIStreamRelease","AVIStreamRelease function [Windows Multimedia]","_win32_AVIStreamRelease","multimedia.avistreamrelease","vfw/AVIStreamRelease"]
old-location: multimedia\avistreamrelease.htm
tech.root: Multimedia
ms.assetid: bd71ddf6-9d02-463d-9d1c-50605441ad59
ms.date: 12/05/2018
ms.keywords: AVIStreamRelease, AVIStreamRelease function [Windows Multimedia], _win32_AVIStreamRelease, multimedia.avistreamrelease, vfw/AVIStreamRelease
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
 - AVIStreamRelease
 - vfw/AVIStreamRelease
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIStreamRelease
---

# AVIStreamRelease function


## -description

The <b>AVIStreamRelease</b> function decrements the reference count of an AVI stream interface handle, and closes the stream if the count reaches zero.



This function supersedes the obsolete <b>AVIStreamClose</b> function.

## -parameters

### -param pavi

Handle to an open stream.

## -returns

Returns the current reference count of the stream. This value should be used only for debugging purposes.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>