---
UID: NF:vfw.IAVIFile.WriteData
title: IAVIFile::WriteData (vfw.h)
description: The WriteData method writes file headers. Called when an application uses the AVIFileWriteData function.
helpviewer_keywords: ["IAVIFile interface [Windows Multimedia]","WriteData method","IAVIFile.WriteData","IAVIFile::WriteData","WriteData","WriteData method [Windows Multimedia]","WriteData method [Windows Multimedia]","IAVIFile interface","_win32_IAVIFile_WriteData","multimedia.iavifile_writedata","vfw/IAVIFile::WriteData"]
old-location: multimedia\iavifile_writedata.htm
tech.root: Multimedia
ms.assetid: 0b693a98-a91a-4fba-99da-e3bac71c1b22
ms.date: 12/05/2018
ms.keywords: IAVIFile interface [Windows Multimedia],WriteData method, IAVIFile.WriteData, IAVIFile::WriteData, WriteData, WriteData method [Windows Multimedia], WriteData method [Windows Multimedia],IAVIFile interface, _win32_IAVIFile_WriteData, multimedia.iavifile_writedata, vfw/IAVIFile::WriteData
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
 - IAVIFile::WriteData
 - vfw/IAVIFile::WriteData
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
 - IAVIFile.WriteData
---

# IAVIFile::WriteData


## -description

The <b>WriteData</b> method writes file headers. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avifilewritedata">AVIFileWriteData</a> function.

## -parameters

### -param ckid

A chunk ID.

### -param lpData

A pointer specifying the memory from which the data is written.

### -param cbData

A LONG specifying the number of bytes to write.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>WriteData</b> has the following syntax:


```cpp

HRESULT WriteData(DWORD fcc, LPVOID lpBuffer, LONG cbBuffer); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>