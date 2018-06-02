---
UID: TP:gdi
ms.assetid: b0acbb78-a6c0-3233-bb9d-d551a85f207d
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Windows GDI



Overview of the Windows GDI technology.

To develop Windows GDI, you need these headers:

 * [fontsub.h](..\fontsub\index.md)
 * [mmsystem.h](..\mmsystem\index.md)
 * [mxdc.h](..\mxdc\index.md)
 * [prnasnot.h](..\prnasnot\index.md)
 * [prntvpt.h](..\prntvpt\index.md)
 * [t2embapi.h](..\t2embapi\index.md)
 * [tvout.h](..\tvout\index.md)
 * [windef.h](..\windef\index.md)
 * [winspool.h](..\winspool\index.md)

For the programming guide, see [Windows GDI](/windows/desktop/gdi).

## Functions

| Title   | Description   |
| ---- |:---- |
| [CreateFontPackage function](..\fontsub\nf-fontsub-createfontpackage.md) | The CreateFontPackage function creates a subset version of a specified TrueType font, typically in order to pass it to a printer. |
| [MergeFontPackage function](..\fontsub\nf-fontsub-mergefontpackage.md) | The MergeFontPackage function manipulates fonts created by CreateFontPackage. |
| [TTCharToUnicode function](..\t2embapi\nf-t2embapi-ttchartounicode.md) | Converts an array of 8-bit character code values to 16-bit Unicode values. |
| [TTDeleteEmbeddedFont function](..\t2embapi\nf-t2embapi-ttdeleteembeddedfont.md) | Releases memory used by an embedded font, hFontReference. |
| [TTEmbedFont function](..\t2embapi\nf-t2embapi-ttembedfont.md) | Creates a font structure containing the subsetted wide-character (16-bit) font. The current font of the device context (hDC) provides the font information. |
| [TTEmbedFontEx function](..\t2embapi\nf-t2embapi-ttembedfontex.md) | Creates a font structure containing the subsetted UCS-4 character (32-bit) font. The current font of the device context (hDC) provides the font information. |
| [TTEmbedFontFromFileA function](..\t2embapi\nf-t2embapi-ttembedfontfromfilea.md) | Creates a font structure containing the subsetted wide-character (16-bit) font. An external file provides the font information. |
| [TTEnableEmbeddingForFacename function](..\t2embapi\nf-t2embapi-ttenableembeddingforfacename.md) | Adds or removes facenames from the typeface exclusion list. |
| [TTGetEmbeddedFontInfo function](..\t2embapi\nf-t2embapi-ttgetembeddedfontinfo.md) | Retrieves information about an embedded font, such as embedding permissions. TTGetEmbeddedFontInfo performs the same task as TTLoadEmbeddedFont but does not allocate internal data structures for the embedded font. |
| [TTGetEmbeddingType function](..\t2embapi\nf-t2embapi-ttgetembeddingtype.md) | Obtains the embedding privileges of a font. |
| [TTGetNewFontName function](..\t2embapi\nf-t2embapi-ttgetnewfontname.md) | Obtains the family name for the font loaded through TTLoadEmbeddedFont. |
| [TTIsEmbeddingEnabled function](..\t2embapi\nf-t2embapi-ttisembeddingenabled.md) | Determines whether the typeface exclusion list contains a specified font. |
| [TTIsEmbeddingEnabledForFacename function](..\t2embapi\nf-t2embapi-ttisembeddingenabledforfacename.md) | Determines whether embedding is enabled for a specified font. |
| [TTLoadEmbeddedFont function](..\t2embapi\nf-t2embapi-ttloadembeddedfont.md) | Reads an embedded font from the document stream and installs it. Also allows a client to further restrict embedding privileges of the font. |
| [TTRunValidationTests function](..\t2embapi\nf-t2embapi-ttrunvalidationtests.md) | Validates part or all glyph data of a wide-character (16-bit) font, in the size range specified. |
| [TTRunValidationTestsEx function](..\t2embapi\nf-t2embapi-ttrunvalidationtestsex.md) | Validates part or all glyph data of a UCS-4 character (32-bit) font, in the size range specified. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [CFP_ALLOCPROC callback function](..\fontsub\nc-fontsub-cfp_allocproc.md) | Client-provided callback function, used by CreateFontPackage and MergeFontPackage to allocate memory. |
| [CFP_FREEPROC callback function](..\fontsub\nc-fontsub-cfp_freeproc.md) | Client-provided callback function, used by CreateFontPackage and MergeFontPackage to free memory. |
| [CFP_REALLOCPROC callback function](..\fontsub\nc-fontsub-cfp_reallocproc.md) | Client-provided callback function, used by CreateFontPackage and MergeFontPackage to reallocate memory when the size of an allocated buffer needs to change. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [TTEMBEDINFO structure](..\t2embapi\ns-t2embapi-ttembedinfo.md) | The TTEMBEDINFO structure contains a list of URLs from which the embedded font object may be legitimately referenced. |
| [TTLOADINFO structure](..\t2embapi\ns-t2embapi-ttloadinfo.md) | The TTLOADINFO structure contains the URL from which the embedded font object has been obtained. |
| [TTVALIDATIONTESTSPARAMS structure](..\t2embapi\ns-t2embapi-ttvalidationtestsparams.md) | The TTVALIDATIONTESTSPARAMS structure contains parameters for testing a Microsoft OpenType font. |
| [TTVALIDATIONTESTSPARAMSEX structure](..\t2embapi\ns-t2embapi-ttvalidationtestsparamsex.md) | The TTVALIDATIONTESTSPARAMSEX structure contains parameters for testing a Microsoft OpenType font. |

## Macros

| Title   | Description   |
| ---- |:---- |
| [DIBINDEX macro](..\mmsystem\nf-mmsystem-dibindex.md) | The DIBINDEX macro takes an index to an entry in a DIB color table and returns a COLORREF value that specifies the color associated with the given index. |
