---
UID: NS:wininet.GOPHER_FIND_DATAA
title: GOPHER_FIND_DATAA (wininet.h)
description: Contains information retrieved by the GopherFindFirstFile and InternetFindNextFile functions. (ANSI)
helpviewer_keywords: ["*LPGOPHER_FIND_DATAA","GOPHER_FIND_DATA","GOPHER_FIND_DATA structure [WinINet]","GOPHER_FIND_DATAA","GOPHER_FIND_DATAW","GOPHER_TYPE_ASK","GOPHER_TYPE_BINARY","GOPHER_TYPE_BITMAP","GOPHER_TYPE_CALENDAR","GOPHER_TYPE_CSO","GOPHER_TYPE_DIRECTORY","GOPHER_TYPE_DOS_ARCHIVE","GOPHER_TYPE_ERROR","GOPHER_TYPE_GIF","GOPHER_TYPE_GOPHER_PLUS","GOPHER_TYPE_HTML","GOPHER_TYPE_IMAGE","GOPHER_TYPE_INDEX_SERVER","GOPHER_TYPE_INLINE","GOPHER_TYPE_MAC_BINHEX","GOPHER_TYPE_MOVIE","GOPHER_TYPE_PDF","GOPHER_TYPE_REDUNDANT","GOPHER_TYPE_SOUND","GOPHER_TYPE_TELNET","GOPHER_TYPE_TEXT_FILE","GOPHER_TYPE_TN3270","GOPHER_TYPE_UNIX_UUENCODED","GOPHER_TYPE_UNKNOWN","LPGOPHER_FIND_DATA","LPGOPHER_FIND_DATA structure pointer [WinINet]","_win32_gopher_find_data","wininet.gopher_find_data","wininet/GOPHER_FIND_DATA","wininet/GOPHER_FIND_DATAA","wininet/GOPHER_FIND_DATAW","wininet/LPGOPHER_FIND_DATA"]
old-location: wininet\gopher_find_data.htm
tech.root: wininet
ms.assetid: 53bcba70-2d6a-465a-86ec-4b11b1474ee1
ms.date: 12/05/2018
ms.keywords: '*LPGOPHER_FIND_DATAA, GOPHER_FIND_DATA, GOPHER_FIND_DATA structure [WinINet], GOPHER_FIND_DATAA, GOPHER_FIND_DATAW, GOPHER_TYPE_ASK, GOPHER_TYPE_BINARY, GOPHER_TYPE_BITMAP, GOPHER_TYPE_CALENDAR, GOPHER_TYPE_CSO, GOPHER_TYPE_DIRECTORY, GOPHER_TYPE_DOS_ARCHIVE, GOPHER_TYPE_ERROR, GOPHER_TYPE_GIF, GOPHER_TYPE_GOPHER_PLUS, GOPHER_TYPE_HTML, GOPHER_TYPE_IMAGE, GOPHER_TYPE_INDEX_SERVER, GOPHER_TYPE_INLINE, GOPHER_TYPE_MAC_BINHEX, GOPHER_TYPE_MOVIE, GOPHER_TYPE_PDF, GOPHER_TYPE_REDUNDANT, GOPHER_TYPE_SOUND, GOPHER_TYPE_TELNET, GOPHER_TYPE_TEXT_FILE, GOPHER_TYPE_TN3270, GOPHER_TYPE_UNIX_UUENCODED, GOPHER_TYPE_UNKNOWN, LPGOPHER_FIND_DATA, LPGOPHER_FIND_DATA structure pointer [WinINet], _win32_gopher_find_data, wininet.gopher_find_data, wininet/GOPHER_FIND_DATA, wininet/GOPHER_FIND_DATAA, wininet/GOPHER_FIND_DATAW, wininet/LPGOPHER_FIND_DATA'
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GOPHER_FIND_DATAW (Unicode) and GOPHER_FIND_DATAA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GOPHER_FIND_DATAA, *LPGOPHER_FIND_DATAA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPGOPHER_FIND_DATAA
 - wininet/LPGOPHER_FIND_DATAA
 - GOPHER_FIND_DATAA
 - wininet/GOPHER_FIND_DATAA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - GOPHER_FIND_DATA
 - GOPHER_FIND_DATAA
 - GOPHER_FIND_DATAW
---

# GOPHER_FIND_DATAA structure


## -description

<p class="CCE_Message">[The <b>GOPHER_FIND_DATA</b> structure is available for use in the operating systems specified in the Requirements section.]

Contains information retrieved by the 
<a href="/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a> and 
<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a> functions.

## -struct-fields

### -field DisplayString

Friendly name of an object. An application can display this string to allow the user to select the object.

### -field GopherType

Describes the item returned. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_ASK"></a><a id="gopher_type_ask"></a><dl>
<dt><b>GOPHER_TYPE_ASK</b></dt>
</dl>
</td>
<td width="60%">
Ask+ item. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_BINARY"></a><a id="gopher_type_binary"></a><dl>
<dt><b>GOPHER_TYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_BITMAP"></a><a id="gopher_type_bitmap"></a><dl>
<dt><b>GOPHER_TYPE_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
Bitmap file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_CALENDAR"></a><a id="gopher_type_calendar"></a><dl>
<dt><b>GOPHER_TYPE_CALENDAR</b></dt>
</dl>
</td>
<td width="60%">
Calendar file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_CSO"></a><a id="gopher_type_cso"></a><dl>
<dt><b>GOPHER_TYPE_CSO</b></dt>
</dl>
</td>
<td width="60%">
CSO telephone book server. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_DIRECTORY"></a><a id="gopher_type_directory"></a><dl>
<dt><b>GOPHER_TYPE_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">
Directory of additional Gopher items. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_DOS_ARCHIVE"></a><a id="gopher_type_dos_archive"></a><dl>
<dt><b>GOPHER_TYPE_DOS_ARCHIVE</b></dt>
</dl>
</td>
<td width="60%">
MS-DOS archive file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_ERROR"></a><a id="gopher_type_error"></a><dl>
<dt><b>GOPHER_TYPE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Indicator of an error condition. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_GIF"></a><a id="gopher_type_gif"></a><dl>
<dt><b>GOPHER_TYPE_GIF</b></dt>
</dl>
</td>
<td width="60%">
GIF graphics file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_GOPHER_PLUS"></a><a id="gopher_type_gopher_plus"></a><dl>
<dt><b>GOPHER_TYPE_GOPHER_PLUS</b></dt>
</dl>
</td>
<td width="60%">
Gopher+ item. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_HTML"></a><a id="gopher_type_html"></a><dl>
<dt><b>GOPHER_TYPE_HTML</b></dt>
</dl>
</td>
<td width="60%">
HTML document. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_IMAGE"></a><a id="gopher_type_image"></a><dl>
<dt><b>GOPHER_TYPE_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
Image file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_INDEX_SERVER"></a><a id="gopher_type_index_server"></a><dl>
<dt><b>GOPHER_TYPE_INDEX_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Index server. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_INLINE"></a><a id="gopher_type_inline"></a><dl>
<dt><b>GOPHER_TYPE_INLINE</b></dt>
</dl>
</td>
<td width="60%">
Inline file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_MAC_BINHEX"></a><a id="gopher_type_mac_binhex"></a><dl>
<dt><b>GOPHER_TYPE_MAC_BINHEX</b></dt>
</dl>
</td>
<td width="60%">
Macintosh file in BINHEX format. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_MOVIE"></a><a id="gopher_type_movie"></a><dl>
<dt><b>GOPHER_TYPE_MOVIE</b></dt>
</dl>
</td>
<td width="60%">
Movie file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_PDF"></a><a id="gopher_type_pdf"></a><dl>
<dt><b>GOPHER_TYPE_PDF</b></dt>
</dl>
</td>
<td width="60%">
PDF file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_REDUNDANT"></a><a id="gopher_type_redundant"></a><dl>
<dt><b>GOPHER_TYPE_REDUNDANT</b></dt>
</dl>
</td>
<td width="60%">
Indicator of a duplicated server. The information contained within is a duplicate of the primary server. The primary server is defined as the last directory entry that did not have a GOPHER_TYPE_REDUNDANT type. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_SOUND"></a><a id="gopher_type_sound"></a><dl>
<dt><b>GOPHER_TYPE_SOUND</b></dt>
</dl>
</td>
<td width="60%">
Sound file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_TELNET"></a><a id="gopher_type_telnet"></a><dl>
<dt><b>GOPHER_TYPE_TELNET</b></dt>
</dl>
</td>
<td width="60%">
Telnet server. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_TEXT_FILE"></a><a id="gopher_type_text_file"></a><dl>
<dt><b>GOPHER_TYPE_TEXT_FILE</b></dt>
</dl>
</td>
<td width="60%">
ASCII text file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_TN3270"></a><a id="gopher_type_tn3270"></a><dl>
<dt><b>GOPHER_TYPE_TN3270</b></dt>
</dl>
</td>
<td width="60%">
TN3270 server. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_UNIX_UUENCODED"></a><a id="gopher_type_unix_uuencoded"></a><dl>
<dt><b>GOPHER_TYPE_UNIX_UUENCODED</b></dt>
</dl>
</td>
<td width="60%">
UUENCODED file. 

</td>
</tr>
<tr>
<td width="40%"><a id="GOPHER_TYPE_UNKNOWN"></a><a id="gopher_type_unknown"></a><dl>
<dt><b>GOPHER_TYPE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Item type is unknown. 

</td>
</tr>
</table>

### -field SizeLow

Low 32 bits of the file size.

### -field SizeHigh

High 32 bits of the file size.

### -field LastModificationTime

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time when the file was last modified.

### -field Locator

File locator. An application can pass the locator string to 
<a href="/windows/desktop/api/wininet/nf-wininet-gopheropenfilea">GopherOpenFile</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines GOPHER_FIND_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a>

