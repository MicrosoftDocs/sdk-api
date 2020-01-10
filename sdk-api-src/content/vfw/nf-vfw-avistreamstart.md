---
UID: NF:vfw.AVIStreamStart
title: AVIStreamStart function (vfw.h)
description: The AVIStreamStart function returns the starting sample number for the stream.
old-location: multimedia\avistreamstart.htm
tech.root: Multimedia
ms.assetid: d4c66732-f777-44c7-9d61-88b721e150c1
ms.date: 12/05/2018
ms.keywords: AVIStreamStart, AVIStreamStart function [Windows Multimedia], _win32_AVIStreamStart, multimedia.avistreamstart, vfw/AVIStreamStart
f1_keywords:
- vfw/AVIStreamStart
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
api_name:
- AVIStreamStart
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamStart function


## -description



The <b>AVIStreamStart</b> function returns the starting sample number for the stream.




## -parameters




### -param pavi

Handle to an open stream.


## -returns



Returns the number if successful or -1 otherwise.




## -remarks



The argument <i>pavi</i> is a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
 

 

