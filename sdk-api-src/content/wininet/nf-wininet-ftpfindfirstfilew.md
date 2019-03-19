---
UID: NF:wininet.FtpFindFirstFileW
title: FtpFindFirstFileW function (wininet.h)
author: windows-sdk-content
description: Searches the specified directory of the given FTP session. File and directory entries are returned to the application in the WIN32_FIND_DATA structure.
old-location: wininet\ftpfindfirstfile.htm
tech.root: wininet
ms.assetid: 4f331f99-c52c-4744-a9a7-eeb09803862d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FtpFindFirstFile, FtpFindFirstFile function [WinINet], FtpFindFirstFileA, FtpFindFirstFileW, _inet_ftpfindfirstfile_function, wininet.ftpfindfirstfile, wininet/FtpFindFirstFile, wininet/FtpFindFirstFileA, wininet/FtpFindFirstFileW
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpFindFirstFileW (Unicode) and FtpFindFirstFileA (ANSI)
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
 - FtpFindFirstFile
 - FtpFindFirstFileA
 - FtpFindFirstFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FtpFindFirstFileW function


## -description


Searches the specified directory of the given FTP session. File and directory entries are returned to the application in the 
<a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure.


## -parameters




### -param hConnect [in]

Handle to an FTP session returned from 
<a href="https://msdn.microsoft.com/42b5d733-dccd-4c9d-8820-e358e033077c">InternetConnect</a>.


### -param lpszSearchFile [in]

Pointer to a <b>null</b>-terminated string that specifies a valid directory path or file name for the FTP server's file system. The string can contain wildcards, but no blank spaces are allowed. If the value of 
<i>lpszSearchFile</i> is <b>NULL</b> or if it is an empty string, the function  finds the first file in the current directory on the server.


### -param lpFindFileData [out]

Pointer to a 
<a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure that receives information about the found file or directory.


### -param dwFlags [in]

Controls the behavior of this function. This parameter can be a combination of the following values.

<p class="indent">INTERNET_FLAG_HYPERLINK

<p class="indent">INTERNET_FLAG_NEED_FILE

<p class="indent">INTERNET_FLAG_NO_CACHE_WRITE

<p class="indent">INTERNET_FLAG_RELOAD

<p class="indent">INTERNET_FLAG_RESYNCHRONIZE


### -param dwContext [in]

Pointer to a variable that specifies the application-defined value that associates this search with any application data. This parameter is used only if the application has already called 
<a href="https://msdn.microsoft.com/fe15627b-c77b-45c0-8ff6-02faa8512b57">InternetSetStatusCallback</a> to set up a status callback function.


## -returns



Returns a valid handle for the request if the directory enumeration was started successfully, or returns <b>NULL</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If <b>GetLastError</b> returns ERROR_INTERNET_EXTENDED_ERROR, as in the case where the function finds no matching files, call the 
<a href="https://msdn.microsoft.com/0aa274c5-0aa0-4eb9-8aef-3128e735759d">InternetGetLastResponseInfo</a> function to retrieve the extended error text, as documented in <a href="https://msdn.microsoft.com/ee619803-b2a3-4a99-a3e6-120e147843f7">Handling Errors</a>.




## -remarks



For 
<b>FtpFindFirstFile</b>, file times returned in the 
<a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure are in the local time zone, not in a coordinated universal time (UTC) format.

<b>FtpFindFirstFile</b> is similar to the <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a> function. Note, however, that only one 
<b>FtpFindFirstFile</b> can occur at a time within a given FTP session. The enumerations, therefore, are correlated with the FTP session handle. This is because the FTP protocol allows only a single directory enumeration per session.

After calling 
<b>FtpFindFirstFile</b> and until calling 
<a href="https://msdn.microsoft.com/52b57e3c-3cfe-40bc-b87b-90cf39c5c38d">InternetCloseHandle</a>, the application cannot call 
<b>FtpFindFirstFile</b> again on the given FTP session handle. If a call is made to 
<b>FtpFindFirstFile</b> on that handle, the function  fails with 
<a href="https://msdn.microsoft.com/338bf65f-ebe5-4434-8407-9ab2a4c8d381">ERROR_FTP_TRANSFER_IN_PROGRESS</a>. After the calling application has finished using the 
<b>HINTERNET</b> handle returned by 
<b>FtpFindFirstFile</b>, it must be closed using the 
<a href="https://msdn.microsoft.com/52b57e3c-3cfe-40bc-b87b-90cf39c5c38d">InternetCloseHandle</a> function.

After beginning a directory enumeration with 
<b>FtpFindFirstFile</b>, the 
<a href="https://msdn.microsoft.com/7c53e399-b8a5-4cc0-9ef6-88d9a525d87f">InternetFindNextFile</a> function can be used to continue the enumeration.

Because the FTP protocol provides no standard means of enumerating, some of the common information about files, such as file creation date and time, is not always available or correct. When this happens, 
<b>FtpFindFirstFile</b> and 
<a href="https://msdn.microsoft.com/7c53e399-b8a5-4cc0-9ef6-88d9a525d87f">InternetFindNextFile</a> fill in unavailable information with a best guess based on available information. For example, creation and last access dates are often  the same as the file's modification date.

The application cannot call 
<b>FtpFindFirstFile</b> between calls to 
<a href="https://msdn.microsoft.com/fb44d7bd-7868-4c53-aa4b-608d79c5bc7c">FtpOpenFile</a> and 
<a href="https://msdn.microsoft.com/52b57e3c-3cfe-40bc-b87b-90cf39c5c38d">InternetCloseHandle</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/23763672-765f-4bbc-95c9-c28775e91f3d">FTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

