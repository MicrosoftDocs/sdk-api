---
UID: NF:vfw.IAVIFile.EndRecord
title: IAVIFile::EndRecord (vfw.h)
description: The EndRecord method writes the &quot;REC&quot; chunk in a tightly interleaved AVI file (having a one-to-one interleave factor of audio to video). Called when an application uses the AVIFileEndRecord function.
helpviewer_keywords: ["EndRecord","EndRecord method [Windows Multimedia]","EndRecord method [Windows Multimedia]","IAVIFile interface","IAVIFile interface [Windows Multimedia]","EndRecord method","IAVIFile.EndRecord","IAVIFile::EndRecord","_win32_IAVIFile_EndRecord","multimedia.iavifile_endrecord","vfw/IAVIFile::EndRecord"]
old-location: multimedia\iavifile_endrecord.htm
tech.root: Multimedia
ms.assetid: 43c4edbf-d736-4d85-9726-123f92145134
ms.date: 12/05/2018
ms.keywords: EndRecord, EndRecord method [Windows Multimedia], EndRecord method [Windows Multimedia],IAVIFile interface, IAVIFile interface [Windows Multimedia],EndRecord method, IAVIFile.EndRecord, IAVIFile::EndRecord, _win32_IAVIFile_EndRecord, multimedia.iavifile_endrecord, vfw/IAVIFile::EndRecord
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
 - IAVIFile::EndRecord
 - vfw/IAVIFile::EndRecord
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
 - IAVIFile.EndRecord
---

# IAVIFile::EndRecord


## -description

The <b>EndRecord</b> method writes the "REC" chunk in a tightly interleaved AVI file (having a one-to-one interleave factor of audio to video). Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avifileendrecord">AVIFileEndRecord</a> function.



#### - pf

Pointer to the interface to a file.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

This file handler method is typically not used.

For handlers written in C++, <b>EndRecord</b> has the following syntax:


```cpp

HRESULT EndRecord(VOID); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>
