---
UID: NF:vfw.IAVIFile.GetStream
title: IAVIFile::GetStream (vfw.h)
description: The GetStream method opens a stream by accessing it in a file. Called when an application uses the AVIFileGetStream function.
helpviewer_keywords: ["GetStream","GetStream method [Windows Multimedia]","GetStream method [Windows Multimedia]","IAVIFile interface","IAVIFile interface [Windows Multimedia]","GetStream method","IAVIFile.GetStream","IAVIFile::GetStream","_win32_IAVIFile_GetStream","multimedia.iavifile_getstream","vfw/IAVIFile::GetStream"]
old-location: multimedia\iavifile_getstream.htm
tech.root: Multimedia
ms.assetid: 66ab2d8f-39f5-4eec-a873-c6f554e3b8ff
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [Windows Multimedia], GetStream method [Windows Multimedia],IAVIFile interface, IAVIFile interface [Windows Multimedia],GetStream method, IAVIFile.GetStream, IAVIFile::GetStream, _win32_IAVIFile_GetStream, multimedia.iavifile_getstream, vfw/IAVIFile::GetStream
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
 - IAVIFile::GetStream
 - vfw/IAVIFile::GetStream
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
 - IAVIFile.GetStream
---

# IAVIFile::GetStream


## -description

The <b>GetStream</b> method opens a stream by accessing it in a file. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avifilegetstream">AVIFileGetStream</a> function.

## -parameters

### -param ppStream

Pointer to a buffer that receives a pointer to the interface to a stream.

### -param fccType

Four-character code indicating the type of stream to locate.

### -param lParam

Stream number.


#### - pf

Pointer to the interface to a file.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

It is typically easier to implement this method by creating all of the stream objects in advance by using the <a href="/previous-versions/dd798007(v=vs.85)">IAVIFile::Open</a> method. Then, this method accesses the interface to the specified stream.

Remember to increment the reference count maintained by the <b>AddRef</b> method for the stream when this method is used.

For handlers written in C++, GetStream has the following syntax:


```cpp

HRESULT GetStream(PAVISTREAM *ppStream, 
    DWORD fccType, LONG lParam); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>