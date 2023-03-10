---
UID: NF:vfw.IGetFrame.End
title: IGetFrame::End (vfw.h)
description: The End method ends frame extraction and decompression. Called when an application uses the AVIStreamGetFrameClose function.
helpviewer_keywords: ["End","End method [Windows Multimedia]","End method [Windows Multimedia]","IGetFrame interface","IGetFrame interface [Windows Multimedia]","End method","IGetFrame.End","IGetFrame::End","_win32_IGetFrame_End","multimedia.igetframe_end","vfw/IGetFrame::End"]
old-location: multimedia\igetframe_end.htm
tech.root: Multimedia
ms.assetid: dc5423c7-4f21-4941-adda-6f4665e86210
ms.date: 12/05/2018
ms.keywords: End, End method [Windows Multimedia], End method [Windows Multimedia],IGetFrame interface, IGetFrame interface [Windows Multimedia],End method, IGetFrame.End, IGetFrame::End, _win32_IGetFrame_End, multimedia.igetframe_end, vfw/IGetFrame::End
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetFrame::End
 - vfw/IGetFrame::End
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IGetFrame.End
---

# IGetFrame::End


## -description

The <b>End</b> method ends frame extraction and decompression. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamgetframeclose">AVIStreamGetFrameClose</a> function.



#### - ps

Pointer to the interface to a stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Begin</b> has the following syntax:


```cpp

HRESULT End(VOID); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>
