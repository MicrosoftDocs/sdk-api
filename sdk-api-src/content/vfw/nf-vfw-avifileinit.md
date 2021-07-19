---
UID: NF:vfw.AVIFileInit
title: AVIFileInit function (vfw.h)
description: The AVIFileInit function initializes the AVIFile library.
helpviewer_keywords: ["AVIFileInit","AVIFileInit function [Windows Multimedia]","_win32_AVIFileInit","multimedia.avifileinit","vfw/AVIFileInit"]
old-location: multimedia\avifileinit.htm
tech.root: Multimedia
ms.assetid: 3246a7d2-4b17-413d-b0d5-82146c993f26
ms.date: 12/05/2018
ms.keywords: AVIFileInit, AVIFileInit function [Windows Multimedia], _win32_AVIFileInit, multimedia.avifileinit, vfw/AVIFileInit
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
 - AVIFileInit
 - vfw/AVIFileInit
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
 - AVIFileInit
---

# AVIFileInit function


## -description

The <b>AVIFileInit</b> function initializes the AVIFile library.



The AVIFile library maintains a count of the number of times it is initialized, but not the number of times it was released. Use the <a href="/windows/desktop/api/vfw/nf-vfw-avifileexit">AVIFileExit</a> function to release the AVIFile library and decrement the reference count. Call <b>AVIFileInit</b> before using any other AVIFile functions.

This function supersedes the obsolete <b>AVIStreamInit</b> function.



## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
