---
UID: NF:wingdi.GetEnhMetaFileDescriptionA
title: GetEnhMetaFileDescriptionA function (wingdi.h)
description: The GetEnhMetaFileDescription function retrieves an optional text description from an enhanced-format metafile and copies the string to the specified buffer. (ANSI)
helpviewer_keywords: ["GetEnhMetaFileDescriptionA", "wingdi/GetEnhMetaFileDescriptionA"]
old-location: gdi\getenhmetafiledescription.htm
tech.root: gdi
ms.assetid: 51f4f617-fe53-4463-b222-cb6860d15dd6
ms.date: 12/05/2018
ms.keywords: GetEnhMetaFileDescription, GetEnhMetaFileDescription function [Windows GDI], GetEnhMetaFileDescriptionA, GetEnhMetaFileDescriptionW, _win32_GetEnhMetaFileDescription, gdi.getenhmetafiledescription, wingdi/GetEnhMetaFileDescription, wingdi/GetEnhMetaFileDescriptionA, wingdi/GetEnhMetaFileDescriptionW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetEnhMetaFileDescriptionW (Unicode) and GetEnhMetaFileDescriptionA (ANSI)
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
 - GetEnhMetaFileDescriptionA
 - wingdi/GetEnhMetaFileDescriptionA
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
 - GetEnhMetaFileDescription
 - GetEnhMetaFileDescriptionA
 - GetEnhMetaFileDescriptionW
---

# GetEnhMetaFileDescriptionA function


## -description

The <b>GetEnhMetaFileDescription</b> function retrieves an optional text description from an enhanced-format metafile and copies the string to the specified buffer.

## -parameters

### -param hemf [in]

A handle to the enhanced metafile.

### -param cchBuffer [in]

The size, in characters, of the buffer to receive the data. Only this many characters will be copied.

### -param lpDescription [out]

A pointer to a buffer that receives the optional text description.

## -returns

If the optional text description exists and the buffer pointer is <b>NULL</b>, the return value is the length of the text string, in characters.

If the optional text description exists and the buffer pointer is a valid pointer, the return value is the number of characters copied into the buffer.

If the optional text description does not exist, the return value is zero.

If the function fails, the return value is GDI_ERROR.

## -remarks

The optional text description contains two strings, the first identifying the application that created the enhanced metafile and the second identifying the picture contained in the metafile. The strings are separated by a null character and terminated with two null characters, for example, "XYZ Graphics Editor\0Bald Eagle\0\0" where \0 represents the null character.

Where text arguments must use Unicode characters, use this function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.





> [!NOTE]
> The wingdi.h header defines GetEnhMetaFileDescription as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea">CreateEnhMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>
