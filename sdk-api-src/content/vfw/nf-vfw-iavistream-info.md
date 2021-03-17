---
UID: NF:vfw.IAVIStream.Info
title: IAVIStream::Info (vfw.h)
description: The Info method fills and returns an AVISTREAMINFO structure with information about a stream. Called when an application uses the AVIStreamInfo function.
helpviewer_keywords: ["IAVIStream interface [Windows Multimedia]","Info method","IAVIStream.Info","IAVIStream::Info","Info","Info method [Windows Multimedia]","Info method [Windows Multimedia]","IAVIStream interface","_win32_IAVIStream_Info","multimedia.iavistream_info","vfw/IAVIStream::Info"]
old-location: multimedia\iavistream_info.htm
tech.root: Multimedia
ms.assetid: c58c4d68-4d27-4c3c-a1f6-bdafa3633dae
ms.date: 12/05/2018
ms.keywords: IAVIStream interface [Windows Multimedia],Info method, IAVIStream.Info, IAVIStream::Info, Info, Info method [Windows Multimedia], Info method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_Info, multimedia.iavistream_info, vfw/IAVIStream::Info
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
 - IAVIStream::Info
 - vfw/IAVIStream::Info
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
 - IAVIStream.Info
---

# IAVIStream::Info


## -description

The <b>Info</b> method fills and returns an <a href="/windows/desktop/api/vfw/ns-vfw-avistreaminfoa">AVISTREAMINFO</a> structure with information about a stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreaminfoa">AVIStreamInfo</a> function.

## -parameters

### -param psi

Pointer to an <a href="/windows/desktop/api/vfw/ns-vfw-avistreaminfoa">AVISTREAMINFO</a> structure to contain stream information.

### -param lSize

Size, in bytes, of the structure specified by <i>psi</i>.


#### - ps

Pointer to the interface to a stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

If the buffer allocated is too small for the structure, the <b>Info</b> method should fail the call by returning AVIERR_BUFFERTOOSMALL. Otherwise, it should fill the structure and return its size.

For handlers written in C++, <b>Info</b> has the following syntax:


```cpp

HRESULT Info(AVIFILEINFO *psi, LONG lSize) 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>