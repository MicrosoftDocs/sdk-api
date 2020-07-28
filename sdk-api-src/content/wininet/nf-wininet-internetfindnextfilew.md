---
UID: NF:wininet.InternetFindNextFileW
title: InternetFindNextFileW function (wininet.h)
description: Continues a file search started as a result of a previous call to FtpFindFirstFile.Windows XP and Windows Server 2003 R2 and earlier:  Or continues a file search as a result of a previous call to GopherFindFirstFile.
helpviewer_keywords: ["InternetFindNextFile","InternetFindNextFile function [WinINet]","InternetFindNextFileA","InternetFindNextFileW","_inet_internetfindnextfile_function","wininet.internetfindnextfile","wininet/InternetFindNextFile","wininet/InternetFindNextFileA","wininet/InternetFindNextFileW"]
old-location: wininet\internetfindnextfile.htm
tech.root: wininet
ms.assetid: 7c53e399-b8a5-4cc0-9ef6-88d9a525d87f
ms.date: 12/05/2018
ms.keywords: InternetFindNextFile, InternetFindNextFile function [WinINet], InternetFindNextFileA, InternetFindNextFileW, _inet_internetfindnextfile_function, wininet.internetfindnextfile, wininet/InternetFindNextFile, wininet/InternetFindNextFileA, wininet/InternetFindNextFileW
f1_keywords:
- wininet/InternetFindNextFile
dev_langs:
- c++
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetFindNextFileW (Unicode) and InternetFindNextFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wininet.dll
api_name:
- InternetFindNextFile
- InternetFindNextFileA
- InternetFindNextFileW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InternetFindNextFileW function


## -description


Continues a file search started as a result of a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-ftpfindfirstfilea">FtpFindFirstFile</a>.

<b>Windows XP and Windows Server 2003 R2 and earlier:  </b>Or continues a file search as a result of a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a>.


## -parameters




### -param hFind [in]

Handle returned from either 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-ftpfindfirstfilea">FtpFindFirstFile</a> or  
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a> (directories only).

<b>Windows XP and Windows Server 2003 R2 and earlier:  </b>Also a handle returned from <a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a>.


### -param lpvFindData [out]

Pointer to the buffer that receives information about the  file or directory. The format of the information placed in the buffer depends on the protocol in use. The FTP protocol returns a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure.

<b>Windows XP and Windows Server 2003 R2 and earlier:  </b>The Gopher protocol returns a 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/ns-wininet-gopher_find_dataa">GOPHER_FIND_DATA</a> structure.


## -returns



Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the function finds no matching files, 
<b>GetLastError</b> returns <b>ERROR_NO_MORE_FILES</b>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetFindNextFile as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
 

 

