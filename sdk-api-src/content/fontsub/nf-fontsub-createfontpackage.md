---
UID: NF:fontsub.CreateFontPackage
title: CreateFontPackage function (fontsub.h)
description: The CreateFontPackage function creates a subset version of a specified TrueType font, typically in order to pass it to a printer.
helpviewer_keywords: ["CreateFontPackage","CreateFontPackage function [Windows GDI]","TTFCFP_APPLE_PLATFORMID","TTFCFP_DELTA","TTFCFP_DONT_CARE","TTFCFP_FLAGS_COMPRESS","TTFCFP_FLAGS_GLYPHLIST","TTFCFP_FLAGS_SUBSET","TTFCFP_FLAGS_TTC","TTFCFP_ISO_PLATFORMID","TTFCFP_MS_PLATFORMID","TTFCFP_STD_MAC_CHAR_SET","TTFCFP_SUBSET","TTFCFP_SUBSET1","TTFCFP_SYMBOL_CHAR_SET","TTFCFP_UNICODE_CHAR_SET","TTFCFP_UNICODE_PLATFORMID","_win32_CreateFontPackage","fontsub/CreateFontPackage","gdi.createfontpackage"]
old-location: gdi\createfontpackage.htm
tech.root: gdi
ms.assetid: aeea47c7-af55-46c4-b701-e00ec7540d24
ms.date: 12/05/2018
ms.keywords: CreateFontPackage, CreateFontPackage function [Windows GDI], TTFCFP_APPLE_PLATFORMID, TTFCFP_DELTA, TTFCFP_DONT_CARE, TTFCFP_FLAGS_COMPRESS, TTFCFP_FLAGS_GLYPHLIST, TTFCFP_FLAGS_SUBSET, TTFCFP_FLAGS_TTC, TTFCFP_ISO_PLATFORMID, TTFCFP_MS_PLATFORMID, TTFCFP_STD_MAC_CHAR_SET, TTFCFP_SUBSET, TTFCFP_SUBSET1, TTFCFP_SYMBOL_CHAR_SET, TTFCFP_UNICODE_CHAR_SET, TTFCFP_UNICODE_PLATFORMID, _win32_CreateFontPackage, fontsub/CreateFontPackage, gdi.createfontpackage
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
 - CreateFontPackage
 - fontsub/CreateFontPackage
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
 - CreateFontPackage
---

# CreateFontPackage function


## -description

The <b>CreateFontPackage</b> function creates a subset version of a specified TrueType font, typically in order to pass it to a printer. In order to allow for the fact that pages later in a document may need characters or glyphs that were not used on the first page, this function can create an initial subset font package, then create "Delta" font packages that can be merged with the original subset font package, effectively extending it.

## -parameters

### -param puchSrcBuffer [in]

Points to a buffer containing source TTF or TTC data, describing the font that is to be subsetted.

### -param ulSrcBufferSize [in]

Specifies size of *<i>puchSrcBuffer</i>, in bytes.

### -param ppuchFontPackageBuffer [out]

Points to a variable of type unsigned char*. The <b>CreateFontPackage</b> function will allocate a buffer **<i>puchFontPackageBuffer</i>, using <i>lpfnAllocate</i> and <i>lpfnReAllocate</i>. On successful return, the buffer will contain the subset font or font package. The application is responsible for eventually freeing the buffer.

### -param pulFontPackageBufferSize [out]

Points to an unsigned long, which on successful return will specify the allocated size of buffer **<i>puchFontPackageBuffer</i>.

### -param pulBytesWritten [out]

Points to an unsigned long, which on successful return will specify the number of bytes actually used in buffer **<i>puchFontPackageBuffer</i>.

### -param usFlag [in]

Specifies whether this font should be subsetted, compressed, or both; whether it is a TTF or TTC; and whether*pusSubsetKeepListrepresents character codes or glyph indices. Any combination of the following flags may be specified:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_FLAGS_SUBSET"></a><a id="ttfcfp_flags_subset"></a><dl>
<dt><b>TTFCFP_FLAGS_SUBSET</b></dt>
</dl>
</td>
<td width="60%">
If set, requests subsetting.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_FLAGS_COMPRESS"></a><a id="ttfcfp_flags_compress"></a><dl>
<dt><b>TTFCFP_FLAGS_COMPRESS</b></dt>
</dl>
</td>
<td width="60%">
If set, requests compression. The currently shipping version of this function does not do compression. This flag allows for future implementation of this capability, but is currently ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_FLAGS_TTC"></a><a id="ttfcfp_flags_ttc"></a><dl>
<dt><b>TTFCFP_FLAGS_TTC</b></dt>
</dl>
</td>
<td width="60%">
If set, specifies that the font in <i>puchSrcBuffer</i> is a TTC; otherwise, it must be a TTF.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_FLAGS_GLYPHLIST"></a><a id="ttfcfp_flags_glyphlist"></a><dl>
<dt><b>TTFCFP_FLAGS_GLYPHLIST</b></dt>
</dl>
</td>
<td width="60%">
If set, specifies that*pusSubsetKeepListis a list of glyph indices; otherwise, it must be a list of character codes.

</td>
</tr>
</table>

### -param usTTCIndex [in]

The zero based TTC Index; only used if TTFCFP_FLAGS_TTC is set in <i>usFlags</i>.

### -param usSubsetFormat [in]

The format of the file to create. Select one of these values; they cannot be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_SUBSET"></a><a id="ttfcfp_subset"></a><dl>
<dt><b>TTFCFP_SUBSET</b></dt>
</dl>
</td>
<td width="60%">
Create a standalone Subset font that cannot be merged with later.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_SUBSET1"></a><a id="ttfcfp_subset1"></a><dl>
<dt><b>TTFCFP_SUBSET1</b></dt>
</dl>
</td>
<td width="60%">
Create a Subset font package that can be merged with later.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_DELTA"></a><a id="ttfcfp_delta"></a><dl>
<dt><b>TTFCFP_DELTA</b></dt>
</dl>
</td>
<td width="60%">
Create a Delta font package that can merge with a previous subset font.

</td>
</tr>
</table>

### -param usSubsetLanguage [in]

The language in the Name table to retain. If Set to 0, all languages will be retained. Used only for initial subsetting: that is, used only if <i>usSubsetFormat</i> is either TTFCFP_SUBSET or TTFCFP_SUBSET1, and the TTFCFP_FLAGS_SUBSET flag is set in <i>usFlags</i>.

### -param usSubsetPlatform [in]

In conjunction with <i>usSubsetEncoding</i>, specifies which CMAP to use. Used only if *<i>pusSubsetKeepList</i> is a list of characters: that is, used only if TTFCFP_FLAGS_GLYPHLIST is not set in <i>usFlags</i>. In that case, by this CMAP subtable is applied to <i>pusSubsetKeepList</i> to create a list of glyphs to retain in the output font or font package.

If used, this must take one of the following values; they cannot be combined:

<table>
<tr>
<th>Value
              </th>
<th>Meaning
              </th>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_UNICODE_PLATFORMID"></a><a id="ttfcfp_unicode_platformid"></a><dl>
<dt><b>TTFCFP_UNICODE_PLATFORMID</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_APPLE_PLATFORMID"></a><a id="ttfcfp_apple_platformid"></a><dl>
<dt><b>TTFCFP_APPLE_PLATFORMID</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_ISO_PLATFORMID"></a><a id="ttfcfp_iso_platformid"></a><dl>
<dt><b>TTFCFP_ISO_PLATFORMID</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_MS_PLATFORMID"></a><a id="ttfcfp_ms_platformid"></a><dl>
<dt><b>TTFCFP_MS_PLATFORMID</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

### -param usSubsetEncoding [in]

In conjunction with <i>usSubsetPlatform</i>, specifies which CMAP to use. Used only if *<i>pusSubsetKeepList</i> is a list of characters: that is, used only if TTFCFP_FLAGS_GLYPHLIST is not set in <i>usFlags</i>.

If used, this must take one of the following values; they cannot be combined:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_STD_MAC_CHAR_SET"></a><a id="ttfcfp_std_mac_char_set"></a><dl>
<dt><b>TTFCFP_STD_MAC_CHAR_SET</b></dt>
</dl>
</td>
<td width="60%">
Can be used only if <i>usSubsetPlatform</i> == TTFCFP_APPLE_PLATFORMID.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_SYMBOL_CHAR_SET"></a><a id="ttfcfp_symbol_char_set"></a><dl>
<dt><b>TTFCFP_SYMBOL_CHAR_SET</b></dt>
</dl>
</td>
<td width="60%">
Can be used only if <i>usSubsetPlatform</i> == TTFSUB_MS_PLATFORMID.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_UNICODE_CHAR_SET"></a><a id="ttfcfp_unicode_char_set"></a><dl>
<dt><b>TTFCFP_UNICODE_CHAR_SET</b></dt>
</dl>
</td>
<td width="60%">
Can be used only if <i>usSubsetPlatform</i> == TTFSUB_MS_PLATFORMID.

</td>
</tr>
<tr>
<td width="40%"><a id="TTFCFP_DONT_CARE"></a><a id="ttfcfp_dont_care"></a><dl>
<dt><b>TTFCFP_DONT_CARE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

### -param pusSubsetKeepList [in]

Points to an array of integers which comprise a list of character codes or glyph indices that should be retained in the output font or font package. If this list contains character codes (that is, if TTFCFP_FLAGS_GLYPHLIST is not set in <i>usFlags</i>), this list may be either Unicode or some other type of encoding, depending on the Platform-Encoding CMAP specified by <i>usSubsetPlatform</i> and <i>usSubsetEncoding</i>.

### -param usSubsetListCount [in]

The number of elements in the list *<i>pusSubsetKeepList</i>.

### -param lpfnAllocate [in]

The callback function to allocate initial memory for <i>puchFontPackageBuffer</i> and for temporary buffers.

### -param lpfnReAllocate [in]

The callback function to reallocate memory for <i>puchFontPackageBuffer</i> and for temporary buffers.

### -param lpfnFree [in]

The callback function to free up memory allocated by <i>lpfnAllocate</i> and <i>lpfnReAllocate</i>.

### -param lpvReserved [in]

Must be set to <b>NULL</b>.

## -returns

If the function is successful, returns zero.

Otherwise, returns a nonzero value. See <a href="/windows/desktop/gdi/font-package-function-error-messages">Font-Package Function Error Messages</a> for possible error returns.

## -remarks

By specifying a value of TTFCFP_SUBSET for <i>usSubsetFormat</i>, you can directly create a working font rather than a font package. This does not allow for future merging, but if there is no need for merging, this skips a step in the downstream processing: a font package needs to be converted back to a working font before it can be used.

By specifying a value of TTFCFP_SUBSET1 for <i>usSubsetFormat</i>, you can create a font package that allows later merging. For example, consider the case where an application calls this function at the start of a large print job. Part way through the print job, the application discovers that it needs glyphs that are not in the subset it has built. The application can make another call to <b>CreateFontPackage</b>, this time specifying a value of TTFCFP_DELTA for <i>usSubsetFormat</i>. The printer can use <a href="/windows/desktop/api/fontsub/nf-fontsub-mergefontpackage">MergeFontPackage</a> to merge in these additional glyphs.

A CMAP maps from character encodings to glyphs. If *<i>pusSubsetKeepList</i> is a list of character values, then the application uses parameters <i>usSubsetPlatform</i> and <i>usSubsetEncoding</i> to specify what type of CMAP is being used, so that character values can be mapped to glyphs.

## -see-also

<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_allocproc">CFP_ALLOCPROC</a>



<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_freeproc">CFP_FREEPROC</a>



<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_reallocproc">CFP_REALLOCPROC</a>



<a href="/windows/desktop/api/fontsub/nf-fontsub-mergefontpackage">MergeFontPackage</a>