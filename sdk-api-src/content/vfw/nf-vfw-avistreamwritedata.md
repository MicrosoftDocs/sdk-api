---
UID: NF:vfw.AVIStreamWriteData
title: AVIStreamWriteData function (vfw.h)
description: The AVIStreamWriteData function writes optional header information to the stream.helpviewer_keywords: ["AVIStreamWriteData","AVIStreamWriteData function [Windows Multimedia]","_win32_AVIStreamWriteData","multimedia.avistreamwritedata","vfw/AVIStreamWriteData"]
old-location: multimedia\avistreamwritedata.htm
tech.root: Multimedia
ms.assetid: 2ca91df6-4721-4282-8b88-81e76d2ab94f
ms.date: 12/05/2018
ms.keywords: AVIStreamWriteData, AVIStreamWriteData function [Windows Multimedia], _win32_AVIStreamWriteData, multimedia.avistreamwritedata, vfw/AVIStreamWriteData
f1_keywords:
- vfw/AVIStreamWriteData
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
- AVIStreamWriteData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamWriteData function


## -description



The <b>AVIStreamWriteData</b> function writes optional header information to the stream.




## -parameters




### -param pavi

Handle to an open stream.


### -param fcc

Four-character code identifying the data.


### -param lp

Pointer to a buffer containing the data to write.


### -param cb

Number of bytes of data to write into the stream.


## -returns



Returns zero if successful or an error otherwise. The return value AVIERR_READONLY indicates the file was opened without write access.




## -remarks



Use the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-avistreamwrite">AVIStreamWrite</a> function to write the multimedia content of the stream. Use <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-avifilewritedata">AVIFileWriteData</a> to write data that applies to an entire file.

The argument <i>pavi</i> is a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
 

 

