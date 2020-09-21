---
UID: NF:vfw.IAVIFile.CreateStream
title: IAVIFile::CreateStream (vfw.h)
description: The CreateStream method creates a stream for writing. Called when an application uses the AVIFileCreateStream function.
helpviewer_keywords: ["CreateStream","CreateStream method [Windows Multimedia]","CreateStream method [Windows Multimedia]","IAVIFile interface","IAVIFile interface [Windows Multimedia]","CreateStream method","IAVIFile.CreateStream","IAVIFile::CreateStream","_win32_IAVIFile_CreateStream","multimedia.iavifile_createstream","vfw/IAVIFile::CreateStream"]
old-location: multimedia\iavifile_createstream.htm
tech.root: Multimedia
ms.assetid: 5c922bb0-53ca-4285-861a-4701503b0445
ms.date: 12/05/2018
ms.keywords: CreateStream, CreateStream method [Windows Multimedia], CreateStream method [Windows Multimedia],IAVIFile interface, IAVIFile interface [Windows Multimedia],CreateStream method, IAVIFile.CreateStream, IAVIFile::CreateStream, _win32_IAVIFile_CreateStream, multimedia.iavifile_createstream, vfw/IAVIFile::CreateStream
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
 - IAVIFile::CreateStream
 - vfw/IAVIFile::CreateStream
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
 - IAVIFile.CreateStream
---

# IAVIFile::CreateStream


## -description

The <b>CreateStream</b> method creates a stream for writing. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avifilecreatestream">AVIFileCreateStream</a> function.

## -parameters

### -param ppStream

Pointer to a buffer that receives a pointer to the interface to the new stream.

### -param psi

Pointer to an <a href="/windows/desktop/api/vfw/ns-vfw-avistreaminfoa">AVISTREAMINFO</a> structure defining the stream to create.

## -returns

Returns HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>CreateStream</b> has the following syntax:


```cpp

HRESULT CreateStream(PAVISTREAM *ppstream, 
    AVISTREAMINFO *psi); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>