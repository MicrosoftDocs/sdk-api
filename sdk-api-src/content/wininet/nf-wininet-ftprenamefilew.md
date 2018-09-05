---
UID: NF:wininet.FtpRenameFileW
title: FtpRenameFileW function
author: windows-sdk-content
description: Renames a file stored on the FTP server.
old-location: wininet\ftprenamefile.htm
old-project: WinInet
ms.assetid: 2c46d8bb-aceb-4dd2-be4f-2c418357d4ae
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FtpRenameFile, FtpRenameFile function [WinINet], FtpRenameFileA, FtpRenameFileW, _inet_ftprenamefile_function, wininet.ftprenamefile, wininet/FtpRenameFile, wininet/FtpRenameFileA, wininet/FtpRenameFileW
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
req.unicode-ansi: FtpRenameFileW (Unicode) and FtpRenameFileA (ANSI)
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
 - FtpRenameFile
 - FtpRenameFileA
 - FtpRenameFileW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FtpRenameFileW function


## -description


Renames a file stored on the FTP server.


## -parameters




### -param hConnect [in]

Handle to an FTP session.


### -param lpszExisting [in]

Pointer to a null-terminated string that contains the name of the file to be renamed.


### -param lpszNew [in]

Pointer to a null-terminated string that contains the new name for the remote file.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<i>lpszExisting</i> and 
<i>lpszNew</i> parameters can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/23763672-765f-4bbc-95c9-c28775e91f3d">FTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

