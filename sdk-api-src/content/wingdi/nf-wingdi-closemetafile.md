---
UID: NF:wingdi.CloseMetaFile
title: CloseMetaFile function (wingdi.h)
description: The CloseMetaFile function closes a metafile device context and returns a handle that identifies a Windows-format metafile.
helpviewer_keywords: ["CloseMetaFile","CloseMetaFile function [Windows GDI]","_win32_CloseMetaFile","gdi.closemetafile","wingdi/CloseMetaFile"]
old-location: gdi\closemetafile.htm
tech.root: gdi
ms.assetid: 8e50457a-8ef8-4e71-8c56-38cfb277f57d
ms.date: 12/05/2018
ms.keywords: CloseMetaFile, CloseMetaFile function [Windows GDI], _win32_CloseMetaFile, gdi.closemetafile, wingdi/CloseMetaFile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CloseMetaFile
 - wingdi/CloseMetaFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Metafile-l1-1-1.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - CloseMetaFile
---

# CloseMetaFile function


## -description

The <b>CloseMetaFile</b> function closes a metafile device context and returns a handle that identifies a Windows-format metafile.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="/windows/desktop/api/wingdi/nf-wingdi-closeenhmetafile">CloseEnhMetaFile</a>.</div><div> </div>

## -parameters

### -param hdc [in]

Handle to a metafile device context used to create a Windows-format metafile.

## -returns

If the function succeeds, the return value is a handle to a Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.

## -remarks

To convert a Windows-format metafile into a new enhanced-format metafile, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a> function.

When an application no longer needs the Windows-format metafile handle, it should delete the handle by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-closeenhmetafile">CloseEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-copymetafilea">CopyMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createmetafilea">CreateMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enummetafile">EnumMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getmetafilebitsex">GetMetaFileBitsEx</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playmetafile">PlayMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>