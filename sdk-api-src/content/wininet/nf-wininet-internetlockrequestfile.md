---
UID: NF:wininet.InternetLockRequestFile
title: InternetLockRequestFile function (wininet.h)
description: Places a lock on the file that is being used.
helpviewer_keywords: ["InternetLockRequestFile","InternetLockRequestFile function [WinINet]","_inet_internetlockrequestfile_function","wininet.internetlockrequestfile","wininet/InternetLockRequestFile"]
old-location: wininet\internetlockrequestfile.htm
tech.root: wininet
ms.assetid: 5924d117-1dcd-43d8-817e-02bda302bdd4
ms.date: 12/05/2018
ms.keywords: InternetLockRequestFile, InternetLockRequestFile function [WinINet], _inet_internetlockrequestfile_function, wininet.internetlockrequestfile, wininet/InternetLockRequestFile
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
 - InternetLockRequestFile
 - wininet/InternetLockRequestFile
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
 - InternetLockRequestFile
---

# InternetLockRequestFile function


## -description

Places a lock on the file that is being used.

## -parameters

### -param hInternet [in]

Handle returned by 
the <a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a>, 
<a href="/windows/desktop/api/wininet/nf-wininet-gopheropenfilea">GopherOpenFile</a>, 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a>, or 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a> function.

### -param lphLockRequestInfo [out]

Pointer to a handle that receives the lock request handle.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle passed to 
<i>hInternet</i> was created using 
<a href="/windows/desktop/WinInet/api-flags">INTERNET_FLAG_NO_CACHE_WRITE</a> or 
<a href="/windows/desktop/WinInet/api-flags">INTERNET_FLAG_DONT_CACHE</a>, the function creates a temporary file with the extension .tmp, unless it is an HTTPS resource. If the handle was created using <b>INTERNET_FLAG_NO_CACHE_WRITE</b> or <b>INTERNET_FLAG_DONT_CACHE</b> and it is accessing an HTTPS resource, 
<b>InternetLockRequestFile</b> fails.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetunlockrequestfile">InternetUnlockRequestFile</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>