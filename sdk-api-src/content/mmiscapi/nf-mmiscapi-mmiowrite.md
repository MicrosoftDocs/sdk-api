---
UID: NF:mmiscapi.mmioWrite
title: mmioWrite function
author: windows-sdk-content
description: The mmioWrite function writes a specified number of bytes to a file opened by using the mmioOpen function.
old-location: multimedia\mmiowrite.htm
tech.root: Multimedia
ms.assetid: e47d00ba-ad29-4a23-8a7c-604bedac10e7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_mmioWrite, mmioWrite, mmioWrite function [Windows Multimedia], mmsystem/mmioWrite, multimedia.mmiowrite"
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mmioWrite function


## -description



The <b>mmioWrite</b> function writes a specified number of bytes to a file opened by using the <a href="https://msdn.microsoft.com/7361f0f2-1c3c-49f1-aec1-2927e05ef0f0">mmioOpen</a> function.




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



