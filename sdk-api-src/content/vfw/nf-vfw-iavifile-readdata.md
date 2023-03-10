---
UID: NF:vfw.IAVIFile.ReadData
title: IAVIFile::ReadData (vfw.h)
description: The ReadData method reads file headers. Called when an application uses the AVIFileReadData function.
helpviewer_keywords: ["IAVIFile interface [Windows Multimedia]","ReadData method","IAVIFile.ReadData","IAVIFile::ReadData","ReadData","ReadData method [Windows Multimedia]","ReadData method [Windows Multimedia]","IAVIFile interface","_win32_IAVIFile_ReadData","multimedia.iavifile_readdata","vfw/IAVIFile::ReadData"]
old-location: multimedia\iavifile_readdata.htm
tech.root: Multimedia
ms.assetid: 52071d08-1e95-4b4b-b85c-3fcca2c666aa
ms.date: 12/05/2018
ms.keywords: IAVIFile interface [Windows Multimedia],ReadData method, IAVIFile.ReadData, IAVIFile::ReadData, ReadData, ReadData method [Windows Multimedia], ReadData method [Windows Multimedia],IAVIFile interface, _win32_IAVIFile_ReadData, multimedia.iavifile_readdata, vfw/IAVIFile::ReadData
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
 - IAVIFile::ReadData
 - vfw/IAVIFile::ReadData
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
 - IAVIFile.ReadData
---

# IAVIFile::ReadData


## -description

The <b>ReadData</b> method reads file headers. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avifilereaddata">AVIFileReadData</a> function.

## -parameters

### -param ckid

A chunk identifier.

### -param lpData

A pointer specifying the memory into which the data is read.

### -param lpcbData

A pointer to a LONG specifying the number of bytes read.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>ReadData</b> has the following syntax:


```cpp

HRESULT ReadData(DWORD fcc, LPVOID lp, LONG *lpcb); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>