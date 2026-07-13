---
UID: NF:wingdi.GetEnhMetaFileW
title: GetEnhMetaFileW function (wingdi.h)
description: The GetEnhMetaFile function creates a handle that identifies the enhanced-format metafile stored in the specified file. (Unicode)
helpviewer_keywords: ["GetEnhMetaFile", "GetEnhMetaFile function [Windows GDI]", "GetEnhMetaFileW", "_win32_GetEnhMetaFile", "gdi.getenhmetafile", "wingdi/GetEnhMetaFile", "wingdi/GetEnhMetaFileW"]
old-location: gdi\getenhmetafile.htm
tech.root: gdi
ms.assetid: bcb9611e-8e4e-4f87-8a1e-dedbe0042821
ms.date: 12/05/2018
ms.keywords: GetEnhMetaFile, GetEnhMetaFile function [Windows GDI], GetEnhMetaFileA, GetEnhMetaFileW, _win32_GetEnhMetaFile, gdi.getenhmetafile, wingdi/GetEnhMetaFile, wingdi/GetEnhMetaFileA, wingdi/GetEnhMetaFileW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetEnhMetaFileW (Unicode) and GetEnhMetaFileA (ANSI)
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
 - GetEnhMetaFileW
 - wingdi/GetEnhMetaFileW
dev_langs:
 - c++
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
 - GetEnhMetaFile
 - GetEnhMetaFileA
 - GetEnhMetaFileW
---

# GetEnhMetaFileW function


## -description

The <b>GetEnhMetaFile</b> function creates a handle that identifies the enhanced-format metafile stored in the specified file.

## -parameters

### -param lpName [in]

A pointer to a null-terminated string that specifies the name of an enhanced metafile.

## -returns

If the function succeeds, the return value is a handle to the enhanced metafile.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When the application no longer needs an enhanced-metafile handle, it should delete the handle by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a> function.

A Windows-format metafile must be converted to the enhanced format before it can be processed by the <b>GetEnhMetaFile</b> function. To convert the file, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a> function.

Where text arguments must use Unicode characters, use this function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.


#### Examples

For an example, see <a href="/windows/desktop/gdi/opening-an-enhanced-metafile-and-displaying-its-contents">Opening an Enhanced Metafile and Displaying Its Contents</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines GetEnhMetaFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilea">GetEnhMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>
