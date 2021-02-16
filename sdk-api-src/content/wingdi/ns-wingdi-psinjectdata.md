---
UID: NS:wingdi._PSINJECTDATA
title: PSINJECTDATA (wingdi.h)
description: The PSINJECTDATA structure is a header for the input buffer used with the POSTSCRIPT_INJECTION printer escape function.
helpviewer_keywords: ["*PPSINJECTDATA","PPSINJECTDATA","PPSINJECTDATA structure pointer [Windows GDI]","PSINJECTDATA","PSINJECTDATA structure [Windows GDI]","_win32_PSINJECTDATA_str","gdi.psinjectdata","wingdi/PPSINJECTDATA","wingdi/PSINJECTDATA"]
old-location: gdi\psinjectdata.htm
tech.root: xps
ms.assetid: f42c8f69-7fe9-4740-b295-32ef2a5b714c
ms.date: 12/05/2018
ms.keywords: '*PPSINJECTDATA, PPSINJECTDATA, PPSINJECTDATA structure pointer [Windows GDI], PSINJECTDATA, PSINJECTDATA structure [Windows GDI], _win32_PSINJECTDATA_str, gdi.psinjectdata, wingdi/PPSINJECTDATA, wingdi/PSINJECTDATA'
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
req.typenames: PSINJECTDATA, *PPSINJECTDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PSINJECTDATA
 - wingdi/_PSINJECTDATA
 - PPSINJECTDATA
 - wingdi/PPSINJECTDATA
 - PSINJECTDATA
 - wingdi/PSINJECTDATA
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
 - PSINJECTDATA
---

# PSINJECTDATA structure


## -description

The <b>PSINJECTDATA</b> structure is a header for the input buffer used with the <a href="/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)">POSTSCRIPT_INJECTION</a> printer escape function.

## -struct-fields

### -field DataBytes

The number of bytes of raw data to be injected. The raw data begins immediately following this structure. This size does not include the size of the <b>PSINJECTDATA</b> structure.

### -field InjectionPoint

Specifies where to inject the raw data in the PostScript output. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PSINJECT_BEGINSTREAM</td>
<td>Before the first byte of job stream.</td>
</tr>
<tr>
<td>PSINJECT_PSADOBE</td>
<td>Before %!PS-Adobe.</td>
</tr>
<tr>
<td>PSINJECT_PAGESATEND</td>
<td>Replaces driver's %%Pages (atend).</td>
</tr>
<tr>
<td>PSINJECT_PAGES</td>
<td>Replaces driver's %%Pages nnn.</td>
</tr>
<tr>
<td>PSINJECT_DOCNEEDEDRES</td>
<td>After %%DocumentNeededResources.</td>
</tr>
<tr>
<td>PSINJECT_DOCSUPPLIEDRES</td>
<td>After %%DocumentSuppliedResources.</td>
</tr>
<tr>
<td>PSINJECT_PAGEORDER</td>
<td>Replaces driver's %%PageOrder.</td>
</tr>
<tr>
<td>PSINJECT_ORIENTATION</td>
<td>Replaces driver's %%Orientation.</td>
</tr>
<tr>
<td>PSINJECT_BOUNDINGBOX</td>
<td>Replaces driver's %%BoundingBox.</td>
</tr>
<tr>
<td>PSINJECT_DOCUMENTPROCESSCOLORS</td>
<td>Replaces driver's %%DocumentProcessColors &lt;color&gt;.</td>
</tr>
<tr>
<td>PSINJECT_COMMENTS</td>
<td>Before %%EndComments.</td>
</tr>
<tr>
<td>PSINJECT_BEGINDEFAULTS</td>
<td>After %%BeginDefaults.</td>
</tr>
<tr>
<td>PSINJECT_ENDDEFAULTS</td>
<td>Before %%EndDefaults.</td>
</tr>
<tr>
<td>PSINJECT_BEGINPROLOG</td>
<td>After %%BeginProlog.</td>
</tr>
<tr>
<td>PSINJECT_ENDPROLOG</td>
<td>Before %%EndProlog.</td>
</tr>
<tr>
<td>PSINJECT_BEGINSETUP</td>
<td>After %%BeginSetup.</td>
</tr>
<tr>
<td>PSINJECT_ENDSETUP</td>
<td>Before %%EndSetup.</td>
</tr>
<tr>
<td>PSINJECT_TRAILER</td>
<td>After %%Trailer</td>
</tr>
<tr>
<td>PSINJECT_EOF</td>
<td>After %%EOF</td>
</tr>
<tr>
<td>PSINJECT_ENDSTREAM</td>
<td>After the last byte of job stream</td>
</tr>
<tr>
<td>PSINJECT_DOCUMENTPROCESSCOLORSATEND</td>
<td>Replaces driver's %%DocumentProcessColors (atend)</td>
</tr>
<tr>
<td colspan="2"><b>Page level injection points</b></td>
</tr>
<tr>
<td>PSINJECT_PAGENUMBER</td>
<td>Replaces driver's %%Page</td>
</tr>
<tr>
<td>PSINJECT_BEGINPAGESETUP</td>
<td>After %%BeginPageSetup</td>
</tr>
<tr>
<td>PSINJECT_ENDPAGESETUP</td>
<td>Before %%EndPageSetup</td>
</tr>
<tr>
<td>PSINJECT_PAGETRAILER</td>
<td>After %%PageTrailer</td>
</tr>
<tr>
<td>PSINJECT_PLATECOLOR</td>
<td>Replace driver's %%PlateColor: &lt;color&gt;</td>
</tr>
<tr>
<td>PSINJECT_SHOWPAGE</td>
<td>Before showpage operator</td>
</tr>
<tr>
<td>PSINJECT_PAGEBBOX</td>
<td>Replaces driver's %%PageBoundingBox</td>
</tr>
<tr>
<td>PSINJECT_ENDPAGECOMMENTS</td>
<td>Before %%EndPageComments</td>
</tr>
<tr>
<td>PSINJECT_VMSAVE</td>
<td>Before save operator</td>
</tr>
<tr>
<td>PSINJECT_VMRESTORE</td>
<td>After restore operator</td>
</tr>
</table>

### -field PageNumber

The page number (starting from 1) to which the injection data is applied. Specify zero to apply the injection data to all pages. This member is meaningful only for page level injection points starting from PSINJECT_PAGENUMBER. For other injection points, set <b>PageNumber</b> to zero.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)">POSTSCRIPT_INJECTION</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-structures">Print Spooler API Structures</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>