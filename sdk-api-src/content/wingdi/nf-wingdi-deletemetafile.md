---
UID: NF:wingdi.DeleteMetaFile
title: DeleteMetaFile function (wingdi.h)
description: The DeleteMetaFile function deletes a Windows-format metafile or Windows-format metafile handle.
helpviewer_keywords: ["DeleteMetaFile","DeleteMetaFile function [Windows GDI]","_win32_DeleteMetaFile","gdi.deletemetafile","wingdi/DeleteMetaFile"]
old-location: gdi\deletemetafile.htm
tech.root: gdi
ms.assetid: 51766282-f185-4e29-a36e-1069d9d61f7c
ms.date: 12/05/2018
ms.keywords: DeleteMetaFile, DeleteMetaFile function [Windows GDI], _win32_DeleteMetaFile, gdi.deletemetafile, wingdi/DeleteMetaFile
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
 - DeleteMetaFile
 - wingdi/DeleteMetaFile
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
 - DeleteMetaFile
---

# DeleteMetaFile function


## -description

The <b>DeleteMetaFile</b> function deletes a Windows-format metafile or Windows-format metafile handle.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>.</div><div> </div>

## -parameters

### -param hmf [in]

A handle to a Windows-format metafile.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

If the metafile identified by the <i>hmf</i> parameter is stored in memory (rather than on a disk), its content is lost when it is deleted by using the <b>DeleteMetaFile</b> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-copymetafilea">CopyMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createmetafilea">CreateMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>