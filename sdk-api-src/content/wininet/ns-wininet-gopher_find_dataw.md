---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GOPHER_FIND_DATAW structure


## -description


<p class="CCE_Message">[The <b>GOPHER_FIND_DATA</b> structure is available for use in the operating systems specified in the Requirements section.]

Contains information retrieved by the 
<a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a> and 
<a href="https://msdn.microsoft.com/7c53e399-b8a5-4cc0-9ef6-88d9a525d87f">InternetFindNextFile</a> functions.


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


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time when the file was last modified. 


### -field Locator

File locator. An application can pass the locator string to 
<a href="https://msdn.microsoft.com/2731d573-f981-48ce-a306-bb7e295cefc6">GopherOpenFile</a> or 
<a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a>. 


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a>



<a href="https://msdn.microsoft.com/7c53e399-b8a5-4cc0-9ef6-88d9a525d87f">InternetFindNextFile</a>
 

 

