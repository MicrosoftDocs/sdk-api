---
UID: NF:mmiscapi.mmioSetInfo
title: mmioSetInfo function (mmiscapi.h)
author: windows-sdk-content
description: The mmioSetInfo function updates the information retrieved by the mmioGetInfo function about a file opened by using the mmioOpen function. Use this function to terminate direct buffer access of a file opened for buffered I/O.
old-location: multimedia\mmiosetinfo.htm
tech.root: Multimedia
ms.assetid: 3b46ebd6-15e0-4b16-b967-0271946390db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_mmioSetInfo, mmioSetInfo, mmioSetInfo function [Windows Multimedia], mmsystem/mmioSetInfo, multimedia.mmiosetinfo"
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
 - mmioSetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mmioSetInfo function


## -description



The <b>mmioSetInfo</b> function updates the information retrieved by the <a href="https://msdn.microsoft.com/9ca58586-8cd6-4d74-9cef-f0ae41b24fe3">mmioGetInfo</a> function about a file opened by using the <a href="https://msdn.microsoft.com/7361f0f2-1c3c-49f1-aec1-2927e05ef0f0">mmioOpen</a> function. Use this function to terminate direct buffer access of a file opened for buffered I/O.




## -parameters




### -param hmmio

File handle of the file.


### -param pmmioinfo

TBD


### -param fuInfo

TBD




#### - lpmmioinfo

Pointer to an <a href="https://msdn.microsoft.com/44a46d1c-9c9c-42ee-8a2b-ac5b1bc19560">MMIOINFO</a> structure filled with information by the <a href="https://msdn.microsoft.com/9ca58586-8cd6-4d74-9cef-f0ae41b24fe3">mmioGetInfo</a> function.


#### - wFlags

Reserved; must be zero.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



If you have written to the file I/O buffer, set the MMIO_DIRTY flag in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/44a46d1c-9c9c-42ee-8a2b-ac5b1bc19560">MMIOINFO</a> structure before calling <b>mmioSetInfo</b> to terminate direct buffer access. Otherwise, the buffer will not get flushed to disk.



