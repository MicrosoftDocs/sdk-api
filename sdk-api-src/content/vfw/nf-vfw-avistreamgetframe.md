---
UID: NF:vfw.AVIStreamGetFrame
title: AVIStreamGetFrame function (vfw.h)
description: The AVIStreamGetFrame function returns the address of a decompressed video frame.
old-location: multimedia\avistreamgetframe.htm
tech.root: Multimedia
ms.assetid: 9677efee-4c40-4acd-8911-eedcbee67d6b
ms.date: 12/05/2018
ms.keywords: AVIStreamGetFrame, AVIStreamGetFrame function [Windows Multimedia], _win32_AVIStreamGetFrame, multimedia.avistreamgetframe, vfw/AVIStreamGetFrame
ms.topic: function
f1_keywords:
- vfw/AVIStreamGetFrame
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
- AVIStreamGetFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamGetFrame function


## -description



The <b>AVIStreamGetFrame</b> function returns the address of a decompressed video frame.




## -parameters




### -param pg

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nn-vfw-igetframe">IGetFrame</a> interface.


### -param lPos

Position, in samples, within the stream of the desired frame.


## -returns



Returns a pointer to the frame data if successful or <b>NULL</b> otherwise. The frame data is returned as a packed DIB.




## -remarks



The returned frame is valid only until the next call to this function or the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-avistreamgetframeclose">AVIStreamGetFrameClose</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
 

 

