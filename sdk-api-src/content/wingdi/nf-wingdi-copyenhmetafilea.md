---
UID: NF:wingdi.CopyEnhMetaFileA
title: CopyEnhMetaFileA function (wingdi.h)
description: The CopyEnhMetaFile function copies the contents of an enhanced-format metafile to a specified file. (ANSI)
helpviewer_keywords: ["CopyEnhMetaFileA", "wingdi/CopyEnhMetaFileA"]
old-location: gdi\copyenhmetafile.htm
tech.root: gdi
ms.assetid: 7c428828-b239-41d4-926c-88caa0aa7214
ms.date: 12/05/2018
ms.keywords: CopyEnhMetaFile, CopyEnhMetaFile function [Windows GDI], CopyEnhMetaFileA, CopyEnhMetaFileW, _win32_CopyEnhMetaFile, gdi.copyenhmetafile, wingdi/CopyEnhMetaFile, wingdi/CopyEnhMetaFileA, wingdi/CopyEnhMetaFileW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CopyEnhMetaFileW (Unicode) and CopyEnhMetaFileA (ANSI)
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
 - CopyEnhMetaFileA
 - wingdi/CopyEnhMetaFileA
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
 - CopyEnhMetaFile
 - CopyEnhMetaFileA
 - CopyEnhMetaFileW
---

# CopyEnhMetaFileA function


## -description

The <b>CopyEnhMetaFile</b> function copies the contents of an enhanced-format metafile to a specified file.

## -parameters

### -param hEnh [in]

A handle to the enhanced metafile to be copied.

### -param lpFileName [in]

A pointer to the name of the destination file. If this parameter is <b>NULL</b>, the source metafile is copied to memory.

## -returns

If the function succeeds, the return value is a handle to the copy of the enhanced metafile.

If the function fails, the return value is <b>NULL</b>.

## -remarks

Where text arguments must use Unicode characters, use the <b>CopyEnhMetaFile</b> function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

Applications can use metafiles stored in memory for temporary operations.

When the application no longer needs the enhanced-metafile handle, it should delete the handle by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a> function.





> [!NOTE]
> The wingdi.h header defines CopyEnhMetaFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>
