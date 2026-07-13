---
UID: NS:wingdi._DOCINFOW
title: DOCINFOW (wingdi.h)
description: The DOCINFO structure contains the input and output file names and other information used by the StartDoc function. (Unicode)
helpviewer_keywords: ["*LPDOCINFOW","DOCINFO","DOCINFO structure [Windows GDI]","DOCINFOW","LPDOCINFO","LPDOCINFO structure pointer [Windows GDI]","_win32_DOCINFO_str","gdi.docinfo","wingdi/DOCINFO","wingdi/LPDOCINFO"]
old-location: gdi\docinfo.htm
tech.root: xps
ms.assetid: 329bf0d9-399b-4f64-a029-361ef7558aeb
ms.date: 12/05/2018
ms.keywords: '*LPDOCINFOW, DOCINFO, DOCINFO structure [Windows GDI], DOCINFOW, LPDOCINFO, LPDOCINFO structure pointer [Windows GDI], _win32_DOCINFO_str, gdi.docinfo, wingdi/DOCINFO, wingdi/LPDOCINFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DOCINFOW, *LPDOCINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DOCINFOW
 - wingdi/_DOCINFOW
 - LPDOCINFOW
 - wingdi/LPDOCINFOW
 - DOCINFOW
 - wingdi/DOCINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - DOCINFO
---

# DOCINFOW structure


## -description

The <b>DOCINFO</b> structure contains the input and output file names and other information used by the <a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a> function.

## -struct-fields

### -field cbSize

The size, in bytes, of the structure.

### -field lpszDocName

Pointer to a null-terminated string that specifies the name of the document.

### -field lpszOutput

Pointer to a null-terminated string that specifies the name of an output file. If this pointer is <b>NULL</b>, the output will be sent to the device identified by the device context handle that was passed to the <a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a> function.

### -field lpszDatatype

Pointer to a null-terminated string that specifies the type of data used to record the print job. The legal values for this member can be found by calling <a href="/windows/desktop/printdocs/enumprintprocessordatatypes">EnumPrintProcessorDatatypes</a> and can include such values as raw, emf, or XPS_PASS. This member can be <b>NULL</b>. Note that the requested data type might be ignored.

### -field fwType

Specifies additional information about the print job. This member must be zero or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DI_APPBANDING</td>
<td>Applications that use banding should set this flag for optimal performance during printing.</td>
</tr>
<tr>
<td>DI_ROPS_READ_DESTINATION</td>
<td>The application will use raster operations that involve reading from the destination surface.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/printdocs/printing-and-print-spooler-structures">Print Spooler API Structures</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a>

## -remarks

> [!NOTE]
> The wingdi.h header defines DOCINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
