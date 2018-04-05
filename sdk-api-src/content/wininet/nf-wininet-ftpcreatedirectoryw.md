---
UID: NF:wininet.FtpCreateDirectoryW
title: FtpCreateDirectoryW function
author: windows-driver-content
description: Creates a new directory on the FTP server.
old-location: wininet\ftpcreatedirectory.htm
old-project: WinInet
ms.assetid: 51a33c5b-4e82-4148-8a3f-0cf7c0a8bac0
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: FtpCreateDirectory, FtpCreateDirectory function [WinINet], FtpCreateDirectoryA, FtpCreateDirectoryW, _inet_ftpcreatedirectory_function, wininet.ftpcreatedirectory, wininet/FtpCreateDirectory, wininet/FtpCreateDirectoryA, wininet/FtpCreateDirectoryW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpCreateDirectoryW (Unicode) and FtpCreateDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	FtpCreateDirectory
-	FtpCreateDirectoryA
-	FtpCreateDirectoryW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FtpCreateDirectoryW function


## -description


Creates a new directory on the FTP server.


## -parameters




### -param hConnect [in]

Handle returned by a previous call to 
<a href="https://msdn.microsoft.com/42b5d733-dccd-4c9d-8820-e358e033077c">InternetConnect</a> using <b>INTERNET_SERVICE_FTP</b>.


### -param lpszDirectory [in]

Pointer to a null-terminated string that contains the name of the directory to be created. This can be either a fully qualified path or a name relative to the current directory.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the error message indicates that the FTP server denied the request to create a directory, use 
<a href="https://msdn.microsoft.com/0aa274c5-0aa0-4eb9-8aef-3128e735759d">InternetGetLastResponseInfo</a> to determine why.




## -remarks



An application should use 
<a href="https://msdn.microsoft.com/1b757061-469b-4c11-9d0d-38b300216221">FtpGetCurrentDirectory</a> to determine the remote site's current working directory instead of assuming that the remote system uses a hierarchical naming scheme for directories.

The 
<i>lpszDirectory</i> parameter can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/23763672-765f-4bbc-95c9-c28775e91f3d">FTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

