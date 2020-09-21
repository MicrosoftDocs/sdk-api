---
UID: NF:wininet.InternetUnlockRequestFile
title: InternetUnlockRequestFile function (wininet.h)
description: Unlocks a file that was locked using InternetLockRequestFile.
helpviewer_keywords: ["InternetUnlockRequestFile","InternetUnlockRequestFile function [WinINet]","_inet_internetunlockrequestfile_function","wininet.internetunlockrequestfile","wininet/InternetUnlockRequestFile"]
old-location: wininet\internetunlockrequestfile.htm
tech.root: wininet
ms.assetid: 356f7277-66ef-450f-ab5a-0303d0b1d807
ms.date: 12/05/2018
ms.keywords: InternetUnlockRequestFile, InternetUnlockRequestFile function [WinINet], _inet_internetunlockrequestfile_function, wininet.internetunlockrequestfile, wininet/InternetUnlockRequestFile
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
 - InternetUnlockRequestFile
 - wininet/InternetUnlockRequestFile
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
 - InternetUnlockRequestFile
---

# InternetUnlockRequestFile function


## -description

Unlocks a file that was locked using 
<a href="/windows/desktop/api/wininet/nf-wininet-internetlockrequestfile">InternetLockRequestFile</a>.

## -parameters

### -param hLockRequestInfo [in]

Handle to a lock request that was returned by 
<a href="/windows/desktop/api/wininet/nf-wininet-internetlockrequestfile">InternetLockRequestFile</a>.

## -returns

Returns TRUE if successful, or FALSE otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>