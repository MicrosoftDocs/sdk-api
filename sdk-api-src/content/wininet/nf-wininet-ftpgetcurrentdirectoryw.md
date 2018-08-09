---
UID: NF:wininet.FtpGetCurrentDirectoryW
title: FtpGetCurrentDirectoryW function
author: windows-sdk-content
description: Retrieves the current directory for the specified FTP session.
old-location: wininet\ftpgetcurrentdirectory.htm
old-project: wininet
ms.assetid: 1b757061-469b-4c11-9d0d-38b300216221
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FtpGetCurrentDirectory, FtpGetCurrentDirectory function [WinINet], FtpGetCurrentDirectoryA, FtpGetCurrentDirectoryW, _inet_ftpgetcurrentdirectory_function, wininet.ftpgetcurrentdirectory, wininet/FtpGetCurrentDirectory, wininet/FtpGetCurrentDirectoryA, wininet/FtpGetCurrentDirectoryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpGetCurrentDirectoryW (Unicode) and FtpGetCurrentDirectoryA (ANSI)
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
 - FtpGetCurrentDirectory
 - FtpGetCurrentDirectoryA
 - FtpGetCurrentDirectoryW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FtpGetCurrentDirectoryW function


## -description


Retrieves the current directory for the specified FTP session.


## -parameters




### -param hConnect [in]

Handle to an FTP session.


### -param lpszCurrentDirectory [out]

Pointer to a null-terminated string that receives the absolute path of the current directory.


### -param lpdwCurrentDirectory [in, out]

Pointer to a variable that specifies the length of the buffer, in <b>TCHARs</b>. The buffer length must include room for a terminating null character. Using a length of <b>MAX_PATH</b> is sufficient for all paths. When the function returns, the variable receives the number of characters copied into the buffer.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the 
<i>lpszCurrentDirectory</i> buffer is not large enough, 
<i>lpdwCurrentDirectory</i> receives the number of bytes required to retrieve the full, current directory name.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/23763672-765f-4bbc-95c9-c28775e91f3d">FTP Sessions</a>



<a href="https://msdn.microsoft.com/1ee21e9e-d113-427e-ab47-86139e6ecad0">FtpSetCurrentDirectory</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

