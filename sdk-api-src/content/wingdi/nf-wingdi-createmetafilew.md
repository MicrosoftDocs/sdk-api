---
UID: NF:wingdi.CreateMetaFileW
title: CreateMetaFileW function (wingdi.h)
description: The CreateMetaFile function creates a device context for a Windows-format metafile. (Unicode)
helpviewer_keywords: ["CreateMetaFile", "CreateMetaFile function [Windows GDI]", "CreateMetaFileW", "_win32_CreateMetaFile", "gdi.createmetafile", "wingdi/CreateMetaFile", "wingdi/CreateMetaFileW"]
old-location: gdi\createmetafile.htm
tech.root: gdi
ms.assetid: 81b3baae-f0e6-4b71-a6de-953ad3376dbd
ms.date: 12/05/2018
ms.keywords: CreateMetaFile, CreateMetaFile function [Windows GDI], CreateMetaFileA, CreateMetaFileW, _win32_CreateMetaFile, gdi.createmetafile, wingdi/CreateMetaFile, wingdi/CreateMetaFileA, wingdi/CreateMetaFileW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateMetaFileW (Unicode) and CreateMetaFileA (ANSI)
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
 - CreateMetaFileW
 - wingdi/CreateMetaFileW
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateMetaFile
 - CreateMetaFileA
 - CreateMetaFileW
---

# CreateMetaFileW function


## -description

The <b>CreateMetaFile</b> function creates a device context for a Windows-format metafile.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea">CreateEnhMetaFile</a>.</div><div> </div>

## -parameters

### -param pszFile [in]

A pointer to the file name for the Windows-format metafile to be created. If this parameter is <b>NULL</b>, the Windows-format metafile is memory based and its contents are lost when it is deleted by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a> function.

## -returns

If the function succeeds, the return value is a handle to the device context for the Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.

## -remarks

Where text arguments must use Unicode characters, use the <b>CreateMetaFile</b> function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

<b>CreateMetaFile</b> is a Windows-format metafile function. This function supports only 16-bit Windows-based applications, which are listed in <a href="/windows/desktop/gdi/windows-format-metafiles">Windows-Format Metafiles</a>. It does not record or play back GDI functions such as <a href="/windows/desktop/api/wingdi/nf-wingdi-polybezier">PolyBezier</a>, which were not part of 16-bit Windows.

The device context created by this function can be used to record GDI output functions in a Windows-format metafile. It cannot be used with GDI query functions such as <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcolor">GetTextColor</a>. When the device context is used with a GDI output function, the return value of that function becomes <b>TRUE</b> if the function is recorded and <b>FALSE</b> otherwise. When an object is selected by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function, only a copy of the object is recorded. The object still belongs to the application.

To create a scalable Windows-format metafile, record the graphics output in the MM_ANISOTROPIC mapping mode. The file cannot contain functions that modify the viewport origin and extents, nor can it contain device-dependent functions such as the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a> function. Once created, the Windows metafile can be scaled and rendered to any output device-format by defining the viewport origin and extents of the picture before playing it.





> [!NOTE]
> The wingdi.h header defines CreateMetaFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-closemetafile">CloseMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea">CreateEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcolor">GetTextColor</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>
