---
UID: NF:wingdi.CopyMetaFileW
title: CopyMetaFileW function (wingdi.h)
description: The CopyMetaFile function copies the content of a Windows-format metafile to the specified file. (Unicode)
helpviewer_keywords: ["CopyMetaFile", "CopyMetaFile function [Windows GDI]", "CopyMetaFileW", "_win32_CopyMetaFile", "gdi.copymetafile", "wingdi/CopyMetaFile", "wingdi/CopyMetaFileW"]
old-location: gdi\copymetafile.htm
tech.root: gdi
ms.assetid: e9f97591-697b-47d0-a748-60fda4d5258c
ms.date: 12/05/2018
ms.keywords: CopyMetaFile, CopyMetaFile function [Windows GDI], CopyMetaFileA, CopyMetaFileW, _win32_CopyMetaFile, gdi.copymetafile, wingdi/CopyMetaFile, wingdi/CopyMetaFileA, wingdi/CopyMetaFileW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CopyMetaFileW (Unicode) and CopyMetaFileA (ANSI)
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
 - CopyMetaFileW
 - wingdi/CopyMetaFileW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CopyMetaFile
 - CopyMetaFileA
 - CopyMetaFileW
---

# CopyMetaFileW function


## -description

The <b>CopyMetaFile</b> function copies the content of a Windows-format metafile to the specified file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="/windows/desktop/api/wingdi/nf-wingdi-copyenhmetafilea">CopyEnhMetaFile</a>.</div><div> </div>

## -parameters

### -param unnamedParam1 [in]

A handle to the source Windows-format metafile.

### -param unnamedParam2 [in]

A pointer to the name of the destination file. If this parameter is <b>NULL</b>, the source metafile is copied to memory.

## -returns

If the function succeeds, the return value is a handle to the copy of the Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.

## -remarks

Where text arguments must use Unicode characters, use this function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

When the application no longer needs the Windows-format metafile handle, it should delete the handle by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a> function.





> [!NOTE]
> The wingdi.h header defines CopyMetaFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>
