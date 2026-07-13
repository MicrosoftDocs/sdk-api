---
UID: NF:wininet.GopherFindFirstFileW
title: GopherFindFirstFileW function (wininet.h)
description: Uses a Gopher locator and search criteria to create a session with the server and locate the requested documents, binary files, index servers, or directory trees. (Unicode)
helpviewer_keywords: ["GopherFindFirstFile", "GopherFindFirstFile function [WinINet]", "GopherFindFirstFileW", "_inet_gopherfindfirstfile_function", "wininet.gopherfindfirstfile", "wininet/GopherFindFirstFile", "wininet/GopherFindFirstFileW"]
old-location: wininet\gopherfindfirstfile.htm
tech.root: wininet
ms.assetid: 801dc601-9d1d-4f7d-acf0-b36ea2314d70
ms.date: 12/05/2018
ms.keywords: GopherFindFirstFile, GopherFindFirstFile function [WinINet], GopherFindFirstFileA, GopherFindFirstFileW, _inet_gopherfindfirstfile_function, wininet.gopherfindfirstfile, wininet/GopherFindFirstFile, wininet/GopherFindFirstFileA, wininet/GopherFindFirstFileW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GopherFindFirstFileW (Unicode) and GopherFindFirstFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GopherFindFirstFileW
 - wininet/GopherFindFirstFileW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - GopherFindFirstFile
 - GopherFindFirstFileA
 - GopherFindFirstFileW
---

# GopherFindFirstFileW function


## -description

<p class="CCE_Message">[The <b>GopherFindFirstFile</b> function is available for use in the operating systems specified in the Requirements section.]

Uses a Gopher locator and search criteria to create a session with the server and locate the requested documents, binary files, index servers, or directory trees.

## -parameters

### -param hConnect [in]

Handle to a Gopher session returned by 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>.

### -param lpszLocator [in]

Pointer to a <b>null</b>-terminated string that contains the name of the item to locate. This can be one of the following: 
					

<ul>
<li>Gopher locator returned by a previous call to this function or the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a> function.</li>
<li><b>NULL</b> pointer or empty string indicating that the topmost information from a Gopher server is being returned.</li>
<li>Locator created by the 
<a href="/windows/desktop/api/wininet/nf-wininet-gophercreatelocatora">GopherCreateLocator</a> function.</li>
</ul>

### -param lpszSearchString [in]

Pointer to a buffer that contains the strings to search, if this request is to an index server. Otherwise, this parameter should be <b>NULL</b>.

### -param lpFindData [out]

Pointer to a 
<a href="/windows/desktop/api/wininet/ns-wininet-gopher_find_dataa">GOPHER_FIND_DATA</a> structure that receives the information retrieved by this function.

### -param dwFlags [in]

Controls the function behavior. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_HYPERLINK</dt>
</dl>
</td>
<td width="60%">
Forces a reload if there was no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NEED_FILE</dt>
</dl>
</td>
<td width="60%">
Causes a temporary file to be created if the file cannot be cached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NO_CACHE_WRITE</dt>
</dl>
</td>
<td width="60%">
Does not add the returned entity to the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_RELOAD</dt>
</dl>
</td>
<td width="60%">
Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_RESYNCHRONIZE</dt>
</dl>
</td>
<td width="60%">
Reloads HTTP resources if the resource has been modified since the last time it was downloaded. All FTP and Gopher resources are reloaded.

</td>
</tr>
</table>

### -param dwContext [in]

Pointer to a variable that contains the application-defined value that associates this search with any application data.

## -returns

Returns a valid search handle if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a>.

## -remarks

<b>GopherFindFirstFile</b> closely resembles the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> function. It creates a connection with a Gopher server, and then returns a single structure containing information about the first Gopher object referenced by the locator string.

After calling 
<b>GopherFindFirstFile</b> to retrieve the first Gopher object in an enumeration, an application can use the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a> function to retrieve subsequent Gopher objects.

After the calling application has finished using the 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle returned by 
<b>GopherFindFirstFile</b>, it must be closed using the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> function.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines GopherFindFirstFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
