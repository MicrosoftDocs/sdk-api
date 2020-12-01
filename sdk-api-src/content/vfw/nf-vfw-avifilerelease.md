---
UID: NF:vfw.AVIFileRelease
title: AVIFileRelease function (vfw.h)
description: The AVIFileRelease function decrements the reference count of an AVI file interface handle and closes the file if the count reaches zero.
helpviewer_keywords: ["AVIFileRelease","AVIFileRelease function [Windows Multimedia]","_win32_AVIFileRelease","multimedia.avifilerelease","vfw/AVIFileRelease"]
old-location: multimedia\avifilerelease.htm
tech.root: Multimedia
ms.assetid: c2f94ca2-b46c-48b0-9c31-92cf2cf75be3
ms.date: 12/05/2018
ms.keywords: AVIFileRelease, AVIFileRelease function [Windows Multimedia], _win32_AVIFileRelease, multimedia.avifilerelease, vfw/AVIFileRelease
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
 - AVIFileRelease
 - vfw/AVIFileRelease
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
 - AVIFileRelease
---

# AVIFileRelease function


## -description

The <b>AVIFileRelease</b> function decrements the reference count of an AVI file interface handle and closes the file if the count reaches zero.



This function supersedes the obsolete <b>AVIFileClose</b> function.

## -parameters

### -param pfile

Handle to an open AVI file.

## -returns

Returns the reference count of the file. This return value should be used only for debugging purposes.

## -remarks

The argument <i>pfile</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>