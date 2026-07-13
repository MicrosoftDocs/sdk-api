---
UID: NF:mmiscapi.mmioSetInfo
title: mmioSetInfo function (mmiscapi.h)
description: The mmioSetInfo function updates the information retrieved by the mmioGetInfo function about a file opened by using the mmioOpen function. Use this function to terminate direct buffer access of a file opened for buffered I/O.
helpviewer_keywords: ["_win32_mmioSetInfo","mmioSetInfo","mmioSetInfo function [Windows Multimedia]","mmsystem/mmioSetInfo","multimedia.mmiosetinfo"]
old-location: multimedia\mmiosetinfo.htm
tech.root: Multimedia
ms.assetid: 3b46ebd6-15e0-4b16-b967-0271946390db
ms.date: 12/05/2018
ms.keywords: _win32_mmioSetInfo, mmioSetInfo, mmioSetInfo function [Windows Multimedia], mmsystem/mmioSetInfo, multimedia.mmiosetinfo
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mmioSetInfo
 - mmiscapi/mmioSetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-mm-io-l1-1-0.dll
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - mmioSetInfo
---

# mmioSetInfo function


## -description

The <b>mmioSetInfo</b> function updates the information retrieved by the <a href="/previous-versions/dd757321(v=vs.85)">mmioGetInfo</a> function about a file opened by using the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function. Use this function to terminate direct buffer access of a file opened for buffered I/O.

## -parameters

### -param hmmio

File handle of the file.

### -param pmmioinfo

Pointer to an <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure filled with information by the <a href="/previous-versions/dd757321(v=vs.85)">mmioGetInfo</a> function.

### -param fuInfo

Reserved; must be zero.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

If you have written to the file I/O buffer, set the MMIO_DIRTY flag in the <b>dwFlags</b> member of the <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure before calling <b>mmioSetInfo</b> to terminate direct buffer access. Otherwise, the buffer will not get flushed to disk.