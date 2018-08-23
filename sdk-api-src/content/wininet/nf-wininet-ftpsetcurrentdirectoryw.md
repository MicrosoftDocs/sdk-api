---
UID: NF:wininet.FtpSetCurrentDirectoryW
title: FtpSetCurrentDirectoryW function
author: windows-sdk-content
description: Changes to a different working directory on the FTP server.
old-location: wininet\ftpsetcurrentdirectory.htm
old-project: WinInet
ms.assetid: 1ee21e9e-d113-427e-ab47-86139e6ecad0
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: FtpSetCurrentDirectory, FtpSetCurrentDirectory function [WinINet], FtpSetCurrentDirectoryA, FtpSetCurrentDirectoryW, _inet_ftpsetcurrentdirectory_function, wininet.ftpsetcurrentdirectory, wininet/FtpSetCurrentDirectory, wininet/FtpSetCurrentDirectoryA, wininet/FtpSetCurrentDirectoryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpSetCurrentDirectoryW (Unicode) and FtpSetCurrentDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - FtpSetCurrentDirectory
 - FtpSetCurrentDirectoryA
 - FtpSetCurrentDirectoryW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FtpSetCurrentDirectoryW function


## -description


Changes to a different working directory on the FTP server.


## -parameters




### -param hConnect [in]

Handle to an FTP session.


### -param lpszDirectory [in]

Pointer to a null-terminated string that contains the name of the directory to become the current working directory. This can be either a fully qualified path or a name relative to the current directory.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the error message indicates that the FTP server denied the request to change a directory, use 
<a href="https://msdn.microsoft.com/0aa274c5-0aa0-4eb9-8aef-3128e735759d">InternetGetLastResponseInfo</a> to determine why.




## -remarks



An application should use 
<a href="https://msdn.microsoft.com/1b757061-469b-4c11-9d0d-38b300216221">FtpGetCurrentDirectory</a> to determine the remote site's current working directory, instead of assuming that the remote system uses a hierarchical naming scheme for directories.

The 
<i>lpszDirectory</i> parameter can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/23763672-765f-4bbc-95c9-c28775e91f3d">FTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

