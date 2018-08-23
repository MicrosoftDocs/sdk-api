---
UID: NF:wininet.FtpGetFileSize
title: FtpGetFileSize function
author: windows-sdk-content
description: Retrieves the file size of the requested FTP resource.
old-location: wininet\ftpgetfilesize.htm
old-project: WinInet
ms.assetid: f6cc696b-55b6-4d21-9401-fbb15062d0b4
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: FtpGetFileSize, FtpGetFileSize function [WinINet], _inet_ftpgetfilesize_function, wininet.ftpgetfilesize, wininet/FtpGetFileSize
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
req.unicode-ansi: 
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
 - FtpGetFileSize
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FtpGetFileSize function


## -description


Retrieves the file size of the requested FTP resource.


## -parameters




### -param hFile [in]

Handle returned from a call to 
<a href="https://msdn.microsoft.com/fb44d7bd-7868-4c53-aa4b-608d79c5bc7c">FtpOpenFile</a>.


### -param lpdwFileSizeHigh [out]

Pointer to the high-order unsigned long integer of the file size of the requested FTP resource.


## -returns



Returns the low-order unsigned long integer of the file size of the requested FTP resource.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/23763672-765f-4bbc-95c9-c28775e91f3d">FTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

