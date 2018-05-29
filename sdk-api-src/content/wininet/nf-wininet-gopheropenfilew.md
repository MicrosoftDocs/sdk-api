---
UID: NF:wininet.GopherOpenFileW
title: GopherOpenFileW function
author: windows-sdk-content
description: Begins reading a Gopher data file from a Gopher server.
old-location: wininet\gopheropenfile.htm
old-project: WinInet
ms.assetid: 2731d573-f981-48ce-a306-bb7e295cefc6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GopherOpenFile, GopherOpenFile function [WinINet], GopherOpenFileA, GopherOpenFileW, _inet_gopheropenfile_function, wininet.gopheropenfile, wininet/GopherOpenFile, wininet/GopherOpenFileA, wininet/GopherOpenFileW
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
req.unicode-ansi: GopherOpenFileW (Unicode) and GopherOpenFileA (ANSI)
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
-	GopherOpenFile
-	GopherOpenFileA
-	GopherOpenFileW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GopherOpenFileW function


## -description


<p class="CCE_Message">[The <b>GopherOpenFile</b> function is available for use in the operating systems specified in the Requirements section.]

Begins reading a Gopher data file from a Gopher server.


## -parameters




### -param hConnect [in]

Handle to a Gopher session returned by 
<a href="https://msdn.microsoft.com/42b5d733-dccd-4c9d-8820-e358e033077c">InternetConnect</a>.


### -param lpszLocator [in]

Pointer to a <b>null</b>-terminated string that specifies the file to be opened. Generally, this locator is returned from a call to 
<a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a> or 
<a href="https://msdn.microsoft.com/7c53e399-b8a5-4cc0-9ef6-88d9a525d87f">InternetFindNextFile</a>. Because the Gopher protocol has no concept of a current directory, the locator is always fully qualified.


### -param lpszView [in]

Pointer to a <b>null</b>-terminated string that describes the view to open if several views of the file exist on the server. If 
<i>lpszView</i> is <b>NULL</b>, the function uses the default file view.


### -param dwFlags [in]

Conditions under which subsequent transfers occur. This parameter can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_HYPERLINK</dt>
</dl>
</td>
<td width="60%">
Forces a reload if there was no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NEED_FILE</dt>
</dl>
</td>
<td width="60%">
Causes a temporary file to be created if the file cannot be cached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NO_CACHE_WRITE</dt>
</dl>
</td>
<td width="60%">
Does not add the returned entity to the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_RELOAD</dt>
</dl>
</td>
<td width="60%">
Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_RESYNCHRONIZE</dt>
</dl>
</td>
<td width="60%">
Reloads HTTP resources if the resource has been modified since the last time it was downloaded. All FTP and Gopher resources are reloaded.

</td>
</tr>
</table>
 


### -param dwContext [in]

Pointer to a variable that contains an application-defined value that associates this operation with any application data.


## -returns



Returns a handle if successful, or <b>NULL</b> if the file cannot be opened. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> or 
<a href="https://msdn.microsoft.com/0aa274c5-0aa0-4eb9-8aef-3128e735759d">InternetGetLastResponseInfo</a>.




## -remarks



<b>GopherOpenFile</b> opens a file at a Gopher server. Because a file cannot actually be opened or locked at a server, this function simply associates location information with a handle that an application can use for file-based operations such as 
<a href="https://msdn.microsoft.com/1ec0fe70-4749-4251-9c58-44efdab74688">InternetReadFile</a> or 
<a href="https://msdn.microsoft.com/c9e95532-8c65-45fb-acd0-a1f09cee2ce2">GopherGetAttribute</a>.

After the calling application has finished using the 
<a href="https://msdn.microsoft.com/8a9788ed-eb25-42cb-b912-8dffa3df1850">HINTERNET</a> handle returned by 
<b>GopherOpenFile</b>, it must be closed using the 
<a href="https://msdn.microsoft.com/52b57e3c-3cfe-40bc-b87b-90cf39c5c38d">InternetCloseHandle</a> function.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

