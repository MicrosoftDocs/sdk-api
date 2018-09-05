---
UID: NF:wininet.FtpDeleteFileA
title: FtpDeleteFileA function
author: windows-sdk-content
description: Deletes a file stored on the FTP server.
old-location: wininet\ftpdeletefile.htm
old-project: WinInet
ms.assetid: 16723c97-fd6f-40c2-844d-fc6d2dcc1a32
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FtpDeleteFile, FtpDeleteFile function [WinINet], FtpDeleteFileA, FtpDeleteFileW, _inet_ftpdeletefile_function, wininet.ftpdeletefile, wininet/FtpDeleteFile, wininet/FtpDeleteFileA, wininet/FtpDeleteFileW
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
req.unicode-ansi: FtpDeleteFileW (Unicode) and FtpDeleteFileA (ANSI)
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
 - FtpDeleteFile
 - FtpDeleteFileA
 - FtpDeleteFileW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FtpDeleteFileA function


## -description


Deletes a file stored on the FTP server.


## -parameters




### -param hConnect [in]

Handle returned by a previous call to 
<a href="https://msdn.microsoft.com/42b5d733-dccd-4c9d-8820-e358e033077c">InternetConnect</a> using <b>INTERNET_SERVICE_FTP</b>.


### -param lpszFileName [in]

Pointer to a null-terminated string that contains the name of the file to be deleted.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<i>lpszFileName</i> parameter can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/23763672-765f-4bbc-95c9-c28775e91f3d">FTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

