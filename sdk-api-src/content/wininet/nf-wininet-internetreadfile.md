---
UID: NF:wininet.InternetReadFile
title: InternetReadFile function (wininet.h)
description: Reads data from a handle opened by the InternetOpenUrl, FtpOpenFile, or HttpOpenRequest function.
helpviewer_keywords: ["InternetReadFile","InternetReadFile function [WinINet]","_inet_internetreadfile_function","wininet.internetreadfile","wininet/InternetReadFile"]
old-location: wininet\internetreadfile.htm
tech.root: wininet
ms.assetid: 1ec0fe70-4749-4251-9c58-44efdab74688
ms.date: 12/05/2018
ms.keywords: InternetReadFile, InternetReadFile function [WinINet], _inet_internetreadfile_function, wininet.internetreadfile, wininet/InternetReadFile
req.header: wininet.h
req.include-header: 
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetReadFile
 - wininet/InternetReadFile
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
 - InternetReadFile
---

# InternetReadFile function


## -description

Reads data from a handle opened by the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a>, 
<a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a>, 
or 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> function.

## -parameters

### -param hFile [in]

Handle returned from a previous call to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a>, 
<a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a>, 
or 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a>.

### -param lpBuffer [out]

Pointer to a buffer that receives the data.

### -param dwNumberOfBytesToRead [in]

Number of bytes to be read.

### -param lpdwNumberOfBytesRead [out]

Pointer to a variable that receives the number of bytes read. 
<b>InternetReadFile</b> sets this value to zero before doing any work or error checking.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. An application can also use 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a> when necessary.

## -remarks

<b>InternetReadFile</b> operates much like the base 
<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> function, with a few exceptions. Typically, 
<b>InternetReadFile</b> retrieves data from an 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle as a sequential stream of bytes. The amount of data to be read for each call to 
<b>InternetReadFile</b> is specified by the 
<i>dwNumberOfBytesToRead</i> parameter and the data is returned in the 
<i>lpBuffer</i> parameter. A normal read retrieves the specified 
<i>dwNumberOfBytesToRead</i> for each call to 
<b>InternetReadFile</b> until the end of the file is reached. To ensure all data is retrieved, an application must continue to call the 
<b>InternetReadFile</b> function until the function returns <b>TRUE</b> and the 
<i>lpdwNumberOfBytesRead</i> parameter equals zero. This is especially important if the requested data is written to the cache, because otherwise the cache will not be properly updated and the file downloaded will not be committed to the cache. Note that caching happens automatically unless the original request to open the data stream set the <b>INTERNET_FLAG_NO_CACHE_WRITE</b> flag.

When an application retrieves a handle using 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a>, WinINet attempts to make all data look like a file download, in an effort to make reading from the Internet easier for the application. For some types of information, such as FTP file directory listings, it converts the data to be returned by  
<b>InternetReadFile</b> to an HTML stream. It does this on a line-by-line basis. For example, it can convert an FTP directory listing to a line of HTML and return this HTML to the application.

WinINet attempts to write the HTML to the 
<i>lpBuffer</i> buffer a line at a time. If the application's buffer is too small to fit at least one line of generated HTML, the error code 
<b>ERROR_INSUFFICIENT_BUFFER</b> is returned as an indication to the application that it needs a larger buffer. Also, converted lines might not completely fill the buffer, so 
<b>InternetReadFile</b> can return with less data in 
<i>lpBuffer</i> than requested. Subsequent reads will retrieve all the converted HTML. The application must again check that all data is retrieved as described previously.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

When running asynchronously, if a call to <b>InternetReadFile</b> does not result in a completed transaction, it will return <i>FALSE</i> and a subsequent call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return <i>ERROR_IO_PENDING</i>. When the transaction is completed the <a href="/windows/desktop/api/wininet/nc-wininet-internet_status_callback">InternetStatusCallback</a> specified in a previous call to   <a href="/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback">InternetSetStatusCallback</a> will be called with <i>INTERNET_STATUS_REQUEST_COMPLETE</i>.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>