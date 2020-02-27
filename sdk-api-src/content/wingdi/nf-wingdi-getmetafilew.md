---
UID: NF:wingdi.GetMetaFileW
title: GetMetaFileW function (wingdi.h)
description: The GetMetaFile function creates a handle that identifies the metafile stored in the specified file.
old-location: gdi\getmetafile.htm
tech.root: gdi
ms.assetid: 56A602C4-AE4D-46DE-B5DA-66A68E3A16BF
ms.date: 12/05/2018
ms.keywords: GetMetaFile, GetMetaFile function [Windows GDI], GetMetaFileA, GetMetaFileW, gdi.getmetafile, wingdi/GetMetaFile, wingdi/GetMetaFileA, wingdi/GetMetaFileW
f1_keywords:
- wingdi/GetMetaFile
dev_langs:
- c++
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetMetaFileW (Unicode) and GetMetaFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Gdi32.dll
- Ext-MS-Win-GDI-Metafile-L1-1-2.dll
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32Full.dll
api_name:
- GetMetaFile
- GetMetaFileA
- GetMetaFileW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMetaFileW function


## -description


<p class="CCE_Message">[GetMetaFile is no longer available for use as of Windows 2000. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilea">GetEnhMetaFile</a>.]

The <b>GetMetaFile</b> function creates a handle that identifies the metafile stored in the specified file.


## -parameters




### -param lpName [in]

A pointer to a null-terminated string that specifies the name of a metafile.


## -returns



If the function succeeds, the return value is a handle to the metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



This function is not implemented in the Win32 API. It is provided for compatibility with 16-bit versions of Windows. In Win32 applications, use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilea">GetEnhMetaFile</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilea">GetEnhMetaFile</a>
 

 

