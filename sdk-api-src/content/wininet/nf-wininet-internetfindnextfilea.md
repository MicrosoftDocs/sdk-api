---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# InternetFindNextFileA function


## -description


Continues a file search started as a result of a previous call to 
<a href="https://msdn.microsoft.com/4f331f99-c52c-4744-a9a7-eeb09803862d">FtpFindFirstFile</a>.

<b>Windows XP and Windows Server 2003 R2 and earlier:  </b>Or continues a file search as a result of a previous call to <a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a>.


## -parameters




### -param hFind [in]

Handle returned from either 
<a href="https://msdn.microsoft.com/4f331f99-c52c-4744-a9a7-eeb09803862d">FtpFindFirstFile</a> or  
<a href="https://msdn.microsoft.com/73f969c3-3fa7-43f5-88c5-ba78e59a8d1c">InternetOpenUrl</a> (directories only).

<b>Windows XP and Windows Server 2003 R2 and earlier:  </b>Also a handle returned from <a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a>.


### -param lpvFindData [out]

Pointer to the buffer that receives information about the  file or directory. The format of the information placed in the buffer depends on the protocol in use. The FTP protocol returns a 
<a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure.

<b>Windows XP and Windows Server 2003 R2 and earlier:  </b>The Gopher protocol returns a 
<a href="https://msdn.microsoft.com/53bcba70-2d6a-465a-86ec-4b11b1474ee1">GOPHER_FIND_DATA</a> structure.


## -returns



Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the function finds no matching files, 
<b>GetLastError</b> returns <b>ERROR_NO_MORE_FILES</b>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/80747c0d-5a09-4ffa-a0ca-b051b82acbf8">Enabling Internet Functionality</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

