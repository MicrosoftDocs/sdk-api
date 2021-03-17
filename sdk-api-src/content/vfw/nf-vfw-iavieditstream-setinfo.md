---
UID: NF:vfw.IAVIEditStream.SetInfo
title: IAVIEditStream::SetInfo (vfw.h)
description: The SetInfo method changes the characteristics of a stream. Called when an application uses the EditStreamSetInfo function.
helpviewer_keywords: ["IAVIEditStream interface [Windows Multimedia]","SetInfo method","IAVIEditStream.SetInfo","IAVIEditStream::SetInfo","SetInfo","SetInfo method [Windows Multimedia]","SetInfo method [Windows Multimedia]","IAVIEditStream interface","_win32_IAVIEditStream_SetInfo","multimedia.iavieditstream_setinfo","vfw/IAVIEditStream::SetInfo"]
old-location: multimedia\iavieditstream_setinfo.htm
tech.root: Multimedia
ms.assetid: 46496c24-cbe0-4234-8683-f39fa58e076b
ms.date: 12/05/2018
ms.keywords: IAVIEditStream interface [Windows Multimedia],SetInfo method, IAVIEditStream.SetInfo, IAVIEditStream::SetInfo, SetInfo, SetInfo method [Windows Multimedia], SetInfo method [Windows Multimedia],IAVIEditStream interface, _win32_IAVIEditStream_SetInfo, multimedia.iavieditstream_setinfo, vfw/IAVIEditStream::SetInfo
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
 - IAVIEditStream::SetInfo
 - vfw/IAVIEditStream::SetInfo
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
 - IAVIEditStream.SetInfo
---

# IAVIEditStream::SetInfo


## -description

The <b>SetInfo</b> method changes the characteristics of a stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-editstreamsetinfoa">EditStreamSetInfo</a> function.

## -parameters

### -param lpInfo

Pointer to an <a href="/windows/desktop/api/vfw/ns-vfw-avistreaminfoa">AVISTREAMINFO</a> structure containing the new stream characteristics.

### -param cbInfo

Size, in bytes, of the buffer.


#### - pavi

Pointer to the interface to a stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>SetInfo</b> has the following syntax:


```cpp

HRESULT SetInfo(AVISTREAMINFO *lpInfo, LONG cbInfo); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>



<a href="/windows/desktop/api/vfw/nf-vfw-editstreamsetinfoa">EditStreamSetInfo</a>