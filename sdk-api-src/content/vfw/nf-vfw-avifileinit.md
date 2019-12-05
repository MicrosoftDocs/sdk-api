---
UID: NF:vfw.AVIFileInit
title: AVIFileInit function (vfw.h)
description: The AVIFileInit function initializes the AVIFile library.
old-location: multimedia\avifileinit.htm
tech.root: Multimedia
ms.assetid: 3246a7d2-4b17-413d-b0d5-82146c993f26
ms.date: 12/05/2018
ms.keywords: AVIFileInit, AVIFileInit function [Windows Multimedia], _win32_AVIFileInit, multimedia.avifileinit, vfw/AVIFileInit
ms.topic: function
f1_keywords:
- vfw/AVIFileInit
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIFileInit function


## -description



The <b>AVIFileInit</b> function initializes the AVIFile library.



The AVIFile library maintains a count of the number of times it is initialized, but not the number of times it was released. Use the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-avifileexit">AVIFileExit</a> function to release the AVIFile library and decrement the reference count. Call <b>AVIFileInit</b> before using any other AVIFile functions.

This function supersedes the obsolete <b>AVIStreamInit</b> function.


## -parameters






## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
 

 

