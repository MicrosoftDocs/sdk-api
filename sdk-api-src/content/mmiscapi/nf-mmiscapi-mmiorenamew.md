---
UID: NF:mmiscapi.mmioRenameW
title: mmioRenameW function
author: windows-sdk-content
description: The mmioRename function renames the specified file.
old-location: multimedia\mmiorename.htm
tech.root: Multimedia
ms.assetid: f47ef581-b3c8-409b-9edf-cbc8cfa04036
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_win32_mmioRename, mmioRename, mmioRename function [Windows Multimedia], mmioRenameA, mmioRenameW, mmsystem/mmioRename, mmsystem/mmioRenameA, mmsystem/mmioRenameW, multimedia.mmiorename"
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
req.unicode-ansi: mmioRenameW (Unicode) and mmioRenameA (ANSI)
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
 - mmioRename
 - mmioRenameA
 - mmioRenameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mmioRenameW function


## -description



The <b>mmioRename</b> function renames the specified file.




## -parameters




### -param pszFileName

TBD


### -param pszNewFileName

TBD


### -param pmmioinfo

TBD


### -param fdwRename

TBD




#### - dwRenameFlags

Flags for the rename operation. This parameter should be set to zero.


#### - lpmmioinfo

Pointer to an <a href="https://msdn.microsoft.com/44a46d1c-9c9c-42ee-8a2b-ac5b1bc19560">MMIOINFO</a> structure containing extra parameters used by <b>mmioRename</b>. If this parameter is not <b>NULL</b>, all unused members of the <b>MMIOINFO</b> structure it references must be set to zero, including the reserved members.


#### - szFilename

Pointer to a string containing the file name of the file to rename.


#### - szNewFilename

Pointer to a string containing the new file name.


## -returns



Returns zero if the file was renamed. Otherwise, returns an error code returned from <b>mmioRename</b> or from the I/O procedure.



