---
UID: NF:vfw.IAVIStreaming.End
title: IAVIStreaming::End (vfw.h)
description: The End method ends the streaming operation. Called when an application uses the AVIStreamEndStreaming function.
helpviewer_keywords: ["End","End method [Windows Multimedia]","End method [Windows Multimedia]","IAVIStreaming interface","IAVIStreaming interface [Windows Multimedia]","End method","IAVIStreaming.End","IAVIStreaming::End","_win32_IAVIStreaming_End","multimedia.iavistreaming_end","vfw/IAVIStreaming::End"]
old-location: multimedia\iavistreaming_end.htm
tech.root: Multimedia
ms.assetid: 5db48b61-5926-41fb-9d0d-f39cba6deec9
ms.date: 12/05/2018
ms.keywords: End, End method [Windows Multimedia], End method [Windows Multimedia],IAVIStreaming interface, IAVIStreaming interface [Windows Multimedia],End method, IAVIStreaming.End, IAVIStreaming::End, _win32_IAVIStreaming_End, multimedia.iavistreaming_end, vfw/IAVIStreaming::End
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
 - IAVIStreaming::End
 - vfw/IAVIStreaming::End
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
 - IAVIStreaming.End
---

# IAVIStreaming::End


## -description

The <b>End</b> method ends the streaming operation. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamendstreaming">AVIStreamEndStreaming</a> function.



#### - ps

Pointer to the interface to a stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>End</b> has the following syntax:


```cpp

HRESULT End(VOID); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>
