---
UID: NF:wingdi.SetEnhMetaFileBits
title: SetEnhMetaFileBits function (wingdi.h)
description: The SetEnhMetaFileBits function creates a memory-based enhanced-format metafile from the specified data.
helpviewer_keywords: ["SetEnhMetaFileBits","SetEnhMetaFileBits function [Windows GDI]","_win32_SetEnhMetaFileBits","gdi.setenhmetafilebits","wingdi/SetEnhMetaFileBits"]
old-location: gdi\setenhmetafilebits.htm
tech.root: gdi
ms.assetid: 0f21ed97-e37f-4b44-a2eb-b8e284b3dc4b
ms.date: 12/05/2018
ms.keywords: SetEnhMetaFileBits, SetEnhMetaFileBits function [Windows GDI], _win32_SetEnhMetaFileBits, gdi.setenhmetafilebits, wingdi/SetEnhMetaFileBits
f1_keywords:
- wingdi/SetEnhMetaFileBits
dev_langs:
- c++
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- gdi32.dll
- Ext-MS-Win-GDI-Metafile-l1-1-0.dll
- Ext-MS-Win-GDI-Metafile-l1-1-1.dll
- ext-ms-win-gdi-metafile-l1-1-2.dll
- GDI32Full.dll
api_name:
- SetEnhMetaFileBits
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetEnhMetaFileBits function


## -description


The <b>SetEnhMetaFileBits</b> function creates a memory-based enhanced-format metafile from the specified data.


## -parameters




### -param nSize [in]

Specifies the size, in bytes, of the data provided.


### -param pb [in]

Pointer to a buffer that contains enhanced-metafile data. (It is assumed that the data in the buffer was obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilebits">GetEnhMetaFileBits</a> function.)


## -returns



If the function succeeds, the return value is a handle to a memory-based enhanced metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When the application no longer needs the enhanced-metafile handle, it should delete the handle by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a> function.

The <b>SetEnhMetaFileBits</b> function does not accept metafile data in the Windows format. To import Windows-format metafiles, use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilebits">GetEnhMetaFileBits</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>
 

 

