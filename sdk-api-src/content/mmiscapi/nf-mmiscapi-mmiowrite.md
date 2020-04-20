---
UID: NF:mmiscapi.mmioWrite
title: mmioWrite function (mmiscapi.h)
description: The mmioWrite function writes a specified number of bytes to a file opened by using the mmioOpen function.helpviewer_keywords: ["_win32_mmioWrite","mmioWrite","mmioWrite function [Windows Multimedia]","mmsystem/mmioWrite","multimedia.mmiowrite"]
old-location: multimedia\mmiowrite.htm
tech.root: Multimedia
ms.assetid: e47d00ba-ad29-4a23-8a7c-604bedac10e7
ms.date: 12/05/2018
ms.keywords: _win32_mmioWrite, mmioWrite, mmioWrite function [Windows Multimedia], mmsystem/mmioWrite, multimedia.mmiowrite
f1_keywords:
- mmiscapi/mmioWrite
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Winmm.dll
- API-MS-Win-mm-misc-l1-1-0.dll
- winmmbase.dll
- API-MS-Win-mm-misc-l1-1-1.dll
api_name:
- mmioWrite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# mmioWrite function


## -description



The <b>mmioWrite</b> function writes a specified number of bytes to a file opened by using the <a href="https://docs.microsoft.com/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function.




## -parameters




### -param hmmio

File handle of the file.


### -param pch

Pointer to the buffer to be written to the file.


### -param cch

Number of bytes to write to the file.


## -returns



Returns the number of bytes actually written. If there is an error writing to the file, the return value is -1.




## -remarks



The current file position is incremented by the number of bytes written.



