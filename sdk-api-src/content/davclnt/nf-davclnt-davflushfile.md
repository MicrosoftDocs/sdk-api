---
UID: NF:davclnt.DavFlushFile
title: DavFlushFile function
author: windows-driver-content
description: Flushes the data from the local version of a remote file to the WebDAV server.
old-location: webdav\davflushfile.htm
old-project: WebDAV
ms.assetid: 0022a5ba-a4b2-4289-91be-db7f52e62f91
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: DavFlushFile, DavFlushFile function [WebDAV], davclnt/DavFlushFile, webdav.davflushfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: davclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTHNEXTSTEP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	netapi32.dll
-	DavHlpr.dll
-	Ext-MS-Win-Rdr-DavHlpr-L1-1-0.dll
api_name:
-	DavFlushFile
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
---

# DavFlushFile function


## -description


Flushes the data from the local version of a remote file to the WebDAV server.


## -parameters




### -param hFile [in]

A handle to an open file on a WebDAV server.

The file handle must have the GENERIC_WRITE access right. For more information, see 
<a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


## -returns



If the function succeeds,  or if <i>hFile</i> is a handle to an encrypted file, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



When an application creates or opens a remote file on a WebDAV server, the WebDAV service downloads the file to the local computer, and the application receives a handle to the open file on the server. Any changes that the application makes to the local file have no effect on the remote file until the file handle is closed  and the local version of the file is uploaded to the server. Because the file handle is closed at the same time that the file is saved to the server, the application cannot check whether the file was saved successfully.

To  avoid this problem, use the  <b>DavFlushFile</b> function to flush the data from the local version of the file to the remote file on the WebDAV server. If the function succeeds, this means that the file was saved successfully.

This function does not flush encrypted files. If <i>hFile</i> is a handle to an encrypted file, <b>DavFlushFile</b> returns ERROR_SUCCESS without flushing the file data.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6">FlushFileBuffers</a>



<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

