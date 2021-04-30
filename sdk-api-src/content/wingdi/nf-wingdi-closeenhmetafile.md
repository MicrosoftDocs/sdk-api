---
UID: NF:wingdi.CloseEnhMetaFile
title: CloseEnhMetaFile function (wingdi.h)
description: The CloseEnhMetaFile function closes an enhanced-metafile device context and returns a handle that identifies an enhanced-format metafile.
helpviewer_keywords: ["CloseEnhMetaFile","CloseEnhMetaFile function [Windows GDI]","_win32_CloseEnhMetaFile","gdi.closeenhmetafile","wingdi/CloseEnhMetaFile"]
old-location: gdi\closeenhmetafile.htm
tech.root: gdi
ms.assetid: 3c4a0d8b-75a5-4729-8c64-476c36d01a90
ms.date: 12/05/2018
ms.keywords: CloseEnhMetaFile, CloseEnhMetaFile function [Windows GDI], _win32_CloseEnhMetaFile, gdi.closeenhmetafile, wingdi/CloseEnhMetaFile
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
 - CloseEnhMetaFile
 - wingdi/CloseEnhMetaFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - CloseEnhMetaFile
---

# CloseEnhMetaFile function


## -description

The <b>CloseEnhMetaFile</b> function closes an enhanced-metafile device context and returns a handle that identifies an enhanced-format metafile.

## -parameters

### -param hdc [in]

Handle to an enhanced-metafile device context.

## -returns

If the function succeeds, the return value is a handle to an enhanced metafile.

If the function fails, the return value is <b>NULL</b>.

## -remarks

An application can use the enhanced-metafile handle returned by the <b>CloseEnhMetaFile</b> function to perform the following tasks:

<ul>
<li>Display a picture stored in an enhanced metafile</li>
<li>Create copies of the enhanced metafile</li>
<li>Enumerate, edit, or copy individual records in the enhanced metafile</li>
<li>Retrieve an optional description of the metafile contents from the enhanced-metafile header</li>
<li>Retrieve a copy of the enhanced-metafile header</li>
<li>Retrieve a binary copy of the enhanced metafile</li>
<li>Enumerate the colors in the optional palette</li>
<li>Convert an enhanced-format metafile into a Windows-format metafile</li>
</ul>
When the application no longer needs the enhanced metafile handle, it should release the handle by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-copyenhmetafilea">CopyEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea">CreateEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilebits">GetEnhMetaFileBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getwinmetafilebits">GetWinMetaFileBits</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafile">PlayEnhMetaFile</a>