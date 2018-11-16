---
UID: NF:mmiscapi.mmioRead
title: mmioRead function
author: windows-sdk-content
description: The mmioRead function reads a specified number of bytes from a file opened by using the mmioOpen function.
old-location: multimedia\mmioread.htm
tech.root: Multimedia
ms.assetid: 1053eb3a-15ea-4a4d-9d26-1ef9cf86a610
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_win32_mmioRead, mmioRead, mmioRead function [Windows Multimedia], mmsystem/mmioRead, multimedia.mmioread"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - mmioRead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- mmioRead
: 
---

# mmioRead function


## -description



The <b>mmioRead</b> function reads a specified number of bytes from a file opened by using the <a href="https://msdn.microsoft.com/7361f0f2-1c3c-49f1-aec1-2927e05ef0f0">mmioOpen</a> function.




## -parameters




### -param hmmio

File handle of the file to be read.


### -param pch

Pointer to a buffer to contain the data read from the file.


### -param cch

Number of bytes to read from the file.


## -returns



Returns the number of bytes actually read. If the end of the file has been reached and no more bytes can be read, the return value is 0. If there is an error reading from the file, the return value is –1.



