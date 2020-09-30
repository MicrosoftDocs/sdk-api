---
UID: NF:wininet.FtpGetFileSize
title: FtpGetFileSize function (wininet.h)
description: Retrieves the file size of the requested FTP resource.
helpviewer_keywords: ["FtpGetFileSize","FtpGetFileSize function [WinINet]","_inet_ftpgetfilesize_function","wininet.ftpgetfilesize","wininet/FtpGetFileSize"]
old-location: wininet\ftpgetfilesize.htm
tech.root: wininet
ms.assetid: f6cc696b-55b6-4d21-9401-fbb15062d0b4
ms.date: 12/05/2018
ms.keywords: FtpGetFileSize, FtpGetFileSize function [WinINet], _inet_ftpgetfilesize_function, wininet.ftpgetfilesize, wininet/FtpGetFileSize
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
 - FtpGetFileSize
 - wininet/FtpGetFileSize
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
 - FtpGetFileSize
---

# FtpGetFileSize function


## -description

Retrieves the file size of the requested FTP resource.

## -parameters

### -param hFile [in]

Handle returned from a call to 
<a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a>.

### -param lpdwFileSizeHigh [out]

Pointer to the high-order unsigned long integer of the file size of the requested FTP resource.

## -returns

Returns the low-order unsigned long integer of the file size of the requested FTP resource.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>