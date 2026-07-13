---
UID: NF:wininet.GopherOpenFileA
title: GopherOpenFileA function (wininet.h)
description: Begins reading a Gopher data file from a Gopher server. (ANSI)
helpviewer_keywords: ["GopherOpenFileA", "wininet/GopherOpenFileA"]
old-location: wininet\gopheropenfile.htm
tech.root: wininet
ms.assetid: 2731d573-f981-48ce-a306-bb7e295cefc6
ms.date: 12/05/2018
ms.keywords: GopherOpenFile, GopherOpenFile function [WinINet], GopherOpenFileA, GopherOpenFileW, _inet_gopheropenfile_function, wininet.gopheropenfile, wininet/GopherOpenFile, wininet/GopherOpenFileA, wininet/GopherOpenFileW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GopherOpenFileW (Unicode) and GopherOpenFileA (ANSI)
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
 - GopherOpenFileA
 - wininet/GopherOpenFileA
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
 - GopherOpenFile
 - GopherOpenFileA
 - GopherOpenFileW
---

# GopherOpenFileA function


## -description

<p class="CCE_Message">[The <b>GopherOpenFile</b> function is available for use in the operating systems specified in the Requirements section.]

Begins reading a Gopher data file from a Gopher server.

## -parameters

### -param hConnect [in]

Handle to a Gopher session returned by 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>.

### -param lpszLocator [in]

Pointer to a <b>null</b>-terminated string that specifies the file to be opened. Generally, this locator is returned from a call to 
<a href="/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a>. Because the Gopher protocol has no concept of a current directory, the locator is always fully qualified.

### -param lpszView [in]

Pointer to a <b>null</b>-terminated string that describes the view to open if several views of the file exist on the server. If 
<i>lpszView</i> is <b>NULL</b>, the function uses the default file view.

### -param dwFlags [in]

Conditions under which subsequent transfers occur. This parameter can be any of the following values.

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

Pointer to a variable that contains an application-defined value that associates this operation with any application data.

## -returns

Returns a handle if successful, or <b>NULL</b> if the file cannot be opened. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a>.

## -remarks

<b>GopherOpenFile</b> opens a file at a Gopher server. Because a file cannot actually be opened or locked at a server, this function simply associates location information with a handle that an application can use for file-based operations such as 
<a href="/windows/desktop/api/wininet/nf-wininet-internetreadfile">InternetReadFile</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-gophergetattributea">GopherGetAttribute</a>.

After the calling application has finished using the 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle returned by 
<b>GopherOpenFile</b>, it must be closed using the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> function.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines GopherOpenFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
