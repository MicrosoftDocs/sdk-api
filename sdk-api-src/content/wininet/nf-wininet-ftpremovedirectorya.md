---
UID: NF:wininet.FtpRemoveDirectoryA
title: FtpRemoveDirectoryA function
author: windows-driver-content
description: Removes the specified directory on the FTP server.
old-location: wininet\ftpremovedirectory.htm
old-project: WinInet
ms.assetid: 4c02af2f-ece8-409a-9c3e-495e1beb80ef
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: FtpRemoveDirectory, FtpRemoveDirectory function [WinINet], FtpRemoveDirectoryA, FtpRemoveDirectoryW, _inet_ftpremovedirectory_function, wininet.ftpremovedirectory, wininet/FtpRemoveDirectory, wininet/FtpRemoveDirectoryA, wininet/FtpRemoveDirectoryW
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
req.unicode-ansi: FtpRemoveDirectoryW (Unicode) and FtpRemoveDirectoryA (ANSI)
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
-	FtpRemoveDirectory
-	FtpRemoveDirectoryA
-	FtpRemoveDirectoryW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FtpRemoveDirectoryA function


## -description


Removes the specified directory on the FTP server.


## -parameters




### -param hConnect [in]

Handle to an FTP session.


### -param lpszDirectory [in]

Pointer to a null-terminated string that contains the name of the directory to be removed. This can be either a fully qualified path or a name relative to the current directory.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the error message indicates that the FTP server denied the request to remove a directory, use 
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



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

