---
UID: NF:fontsub.MergeFontPackage
title: MergeFontPackage function (fontsub.h)
description: The MergeFontPackage function manipulates fonts created by CreateFontPackage.
helpviewer_keywords: ["MergeFontPackage","MergeFontPackage function [Windows GDI]","TTFMFP_DELTA","TTFMFP_SUBSET","TTFMFP_SUBSET1","_win32_MergeFontPackage","fontsub/MergeFontPackage","gdi.mergefontpackage"]
old-location: gdi\mergefontpackage.htm
tech.root: gdi
ms.assetid: c51110a0-286c-4d97-9da5-4186ebf8f9b8
ms.date: 12/05/2018
ms.keywords: MergeFontPackage, MergeFontPackage function [Windows GDI], TTFMFP_DELTA, TTFMFP_SUBSET, TTFMFP_SUBSET1, _win32_MergeFontPackage, fontsub/MergeFontPackage, gdi.mergefontpackage
req.header: fontsub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FontSub.lib
req.dll: FontSub.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MergeFontPackage
 - fontsub/MergeFontPackage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FontSub.dll
api_name:
 - MergeFontPackage
---

# MergeFontPackage function


## -description

The <b>MergeFontPackage</b> function manipulates fonts created by <a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a>. It is slightly more flexible than its name might suggest: it can appropriately handle all of the subset fonts and font packages created by <b>CreateFontPackage</b>. It can turn a font package into a working font, and it can merge a Delta font package into an appropriately prepared working font.

Typically, <a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> creates subset fonts and font packages to pass to a printer or print server; <b>MergeFontPackage</b> runs on that printer or print server.

## -parameters

### -param puchMergeFontBuffer [in]

A pointer to a buffer containing a font to merge with. This is used only when <i>usMode</i> is TTFMFP_DELTA.

### -param ulMergeFontBufferSize [in]

Specifies size of *<i>puchMergeFontBuffer</i>, in bytes.

### -param puchFontPackageBuffer [in]

A pointer to a to buffer containing a font package.

### -param ulFontPackageBufferSize [in]

Specifies size of *<i>puchMergeFontBuffer</i>, in bytes.

### -param ppuchDestBuffer [out]

A pointer to a variable of type unsigned char*. The <b>MergeFontPackage</b> function will allocate a buffer **<i>ppuchDestBuffer</i>, using <i>lpfnAllocate</i> and <i>lpfnReAllocate</i>. On successful return, that buffer will contain the resulting merged or expanded font. The application is responsible for eventually freeing that buffer.

### -param pulDestBufferSize [out]

Points to an unsigned long, which on successful return will specify the allocated size of buffer **<i>ppuchDestBuffer</i>.

### -param pulBytesWritten [out]

Points to an unsigned long, which on successful return will specify the number of bytes actually used in buffer **<i>ppuchDestBuffer</i>.

### -param usMode [in]

Specifies what kind of process to perform. Select one of these values; they cannot be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTFMFP_SUBSET"></a><a id="ttfmfp_subset"></a><dl>
<dt><b>TTFMFP_SUBSET</b></dt>
</dl>
</td>
<td width="60%">
Copies a simple working font; see remarks below.

<i>puchMergeFontBuffer</i> will be ignored; <i>puchFontPackageBuffer</i> should contain a working font created by <a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> with <i>usSubsetFormat</i> set to TTFCFP_SUBSET; this working font will simply be copied to <i>ppuchDestBuffer</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFMFP_SUBSET1"></a><a id="ttfmfp_subset1"></a><dl>
<dt><b>TTFMFP_SUBSET1</b></dt>
</dl>
</td>
<td width="60%">
Turns a font package into a mergeable working font; see remarks below.

<i>puchMergeFontBuffer</i> will be ignored; <i>puchFontPackageBuffer</i> should contain a mergeable working font created by <a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> with <i>usSubsetFormat</i> set to TTFCFP_SUBSET1. The result in **<i>ppuchDestBuffer</i> will be a working font that may be merged with later.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFMFP_DELTA"></a><a id="ttfmfp_delta"></a><dl>
<dt><b>TTFMFP_DELTA</b></dt>
</dl>
</td>
<td width="60%">
Merges a Delta font package into a mergeable working font; see remarks below.

*<i>puchFontPackageBuffer</i> should contain a font package created by <a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> with <i>usSubsetFormat</i> set to TTFCFP_DELTA and <i>puchMergeFontBuffer</i> should contain a font package created by a prior call to <b>MergeFontPackage</b> with <i>usMode</i> set to TTFMFP_SUBSET1 or TTFMFP_DELTA. The resulting merged font in **<i>ppuchDestBuffer</i> will be a working font that may be merged with later.

</td>
</tr>
</table>

### -param lpfnAllocate [in]

The callback function to allocate initial memory for <i>ppuchDestBuffer</i> and for temporary buffers.

### -param lpfnReAllocate [in]

The callback function to reallocate memory for <i>ppuchDestBuffer</i> and for temporary buffers.

### -param lpfnFree [in]

The callback function to free up memory allocated by <i>lpfnAllocate</i> and <i>lpfnReAllocate</i>.

### -param lpvReserved [in]

Must be set to <b>NULL</b>.

## -returns

If the function is successful, returns zero.

Otherwise, returns a nonzero value. See <a href="/windows/desktop/gdi/font-package-function-error-messages">Font-Package Function Error Messages</a> for possible error returns.

## -remarks

This function handles four distinct, related entities, each representing a subset font:

<table>
<tr>
<th>Entity</th>
<th>Produced by</th>
<th>Directly usable as a font</th>
</tr>
<tr>
<td>Simple working font</td>
<td>
<a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> with <i>usSubsetFormat</i> set to TFCFP_SUBSET.</td>
<td>Yes</td>
</tr>
<tr>
<td>Font package</td>
<td>
<a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> with <i>usSubsetFormat</i> set to TTFCFP_SUBSET1.</td>
<td>No</td>
</tr>
<tr>
<td>Delta font package</td>
<td>
<a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> with <i>usSubsetFormat</i> set to TTFCFP_DELTA.</td>
<td>No</td>
</tr>
<tr>
<td>Mergeable working font</td>
<td><b>MergeFontPackage</b> with <i>usMode</i> set to TTFMFP_SUBSET1 or TTFMFP_DELTA.</td>
<td>Yes</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_allocproc">CFP_ALLOCPROC</a>



<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_freeproc">CFP_FREEPROC</a>



<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_reallocproc">CFP_REALLOCPROC</a>



<a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a>