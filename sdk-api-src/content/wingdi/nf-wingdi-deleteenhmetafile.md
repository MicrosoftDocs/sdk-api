---
UID: NF:wingdi.DeleteEnhMetaFile
title: DeleteEnhMetaFile function (wingdi.h)
description: The DeleteEnhMetaFile function deletes an enhanced-format metafile or an enhanced-format metafile handle.
helpviewer_keywords: ["DeleteEnhMetaFile","DeleteEnhMetaFile function [Windows GDI]","DeleteEnhMetaFileW","_win32_DeleteEnhMetaFile","gdi.deleteenhmetafile","wingdi/DeleteEnhMetaFile","wingdi/DeleteEnhMetaFileW"]
old-location: gdi\deleteenhmetafile.htm
tech.root: gdi
ms.assetid: d3b93b3b-fa0b-4480-8348-19919c9e904d
ms.date: 12/05/2018
ms.keywords: DeleteEnhMetaFile, DeleteEnhMetaFile function [Windows GDI], DeleteEnhMetaFileW, _win32_DeleteEnhMetaFile, gdi.deleteenhmetafile, wingdi/DeleteEnhMetaFile, wingdi/DeleteEnhMetaFileW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteEnhMetaFileW (Unicode)
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
 - DeleteEnhMetaFile
 - wingdi/DeleteEnhMetaFile
dev_langs:
 - c++
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
 - DeleteEnhMetaFile
 - DeleteEnhMetaFileW
---

# DeleteEnhMetaFile function


## -description

The <b>DeleteEnhMetaFile</b> function deletes an enhanced-format metafile or an enhanced-format metafile handle.

## -parameters

### -param hmf [in]

A handle to an enhanced metafile.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

If the <i>hemf</i> parameter identifies an enhanced metafile stored in memory, the <b>DeleteEnhMetaFile</b> function deletes the metafile. If <i>hemf</i> identifies a metafile stored on a disk, the function deletes the metafile handle but does not destroy the actual metafile. An application can retrieve the file by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilea">GetEnhMetaFile</a> function.


#### Examples

For an example, see <a href="/windows/desktop/gdi/opening-an-enhanced-metafile-and-displaying-its-contents">Opening an Enhanced Metafile and Displaying Its Contents</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-copyenhmetafilea">CopyEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea">CreateEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilea">GetEnhMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>