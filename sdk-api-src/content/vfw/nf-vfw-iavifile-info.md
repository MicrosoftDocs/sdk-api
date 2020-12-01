---
UID: NF:vfw.IAVIFile.Info
title: IAVIFile::Info (vfw.h)
description: The Info method returns with information about an AVI file. Called when an application uses the AVIFileInfo function.
helpviewer_keywords: ["IAVIFile interface [Windows Multimedia]","Info method","IAVIFile.Info","IAVIFile::Info","Info","Info method [Windows Multimedia]","Info method [Windows Multimedia]","IAVIFile interface","_win32_IAVIFile_Info","multimedia.iavifile_info","vfw/IAVIFile::Info"]
old-location: multimedia\iavifile_info.htm
tech.root: Multimedia
ms.assetid: cac01da4-b979-4386-8fc7-f47a7771e6f4
ms.date: 12/05/2018
ms.keywords: IAVIFile interface [Windows Multimedia],Info method, IAVIFile.Info, IAVIFile::Info, Info, Info method [Windows Multimedia], Info method [Windows Multimedia],IAVIFile interface, _win32_IAVIFile_Info, multimedia.iavifile_info, vfw/IAVIFile::Info
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
 - IAVIFile::Info
 - vfw/IAVIFile::Info
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
 - IAVIFile.Info
---

# IAVIFile::Info


## -description

The <b>Info</b> method returns with information about an AVI file. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avifileinfo">AVIFileInfo</a> function.

## -parameters

### -param pfi

A pointer to an <a href="/windows/desktop/api/vfw/ns-vfw-avifileinfoa">AVIFILEINFO</a> structure. The method fills the structure with information about the file.

### -param lSize

The size, in bytes, of the buffer specified by <i>pfi</i>.


#### - pf

Pointer to the interface to a file.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

If the buffer allocated is too small for the structure, this method should fail the call by returning AVIERR_BUFFERTOOSMALL. Otherwise, it should fill the structure and return its size.

For handlers written in C++, <b>Info</b> has the following syntax:


```cpp

HRESULT Info(AVIFILEINFO *pfi, LONG lSize) 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>