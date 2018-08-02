---
UID: NF:davclnt.DavFlushFile
title: DavFlushFile function
author: windows-sdk-content
description: Flushes the data from the local version of a remote file to the WebDAV server.
old-location: webdav\davflushfile.htm
old-project: webdav
ms.assetid: 0022a5ba-a4b2-4289-91be-db7f52e62f91
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: DavFlushFile, DavFlushFile function [WebDAV], davclnt/DavFlushFile, webdav.davflushfile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUTHNEXTSTEP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - netapi32.dll
 - DavHlpr.dll
 - Ext-MS-Win-Rdr-DavHlpr-L1-1-0.dll
api_name:
 - DavFlushFile
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
<a href="https://msdn.microsoft.com/library/Aa364399(v=VS.85).aspx">File Security and Access Rights</a>.


## -returns



If the function succeeds,  or if <i>hFile</i> is a handle to an encrypted file, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



When an application creates or opens a remote file on a WebDAV server, the WebDAV service downloads the file to the local computer, and the application receives a handle to the open file on the server. Any changes that the application makes to the local file have no effect on the remote file until the file handle is closed  and the local version of the file is uploaded to the server. Because the file handle is closed at the same time that the file is saved to the server, the application cannot check whether the file was saved successfully.

To  avoid this problem, use the  <b>DavFlushFile</b> function to flush the data from the local version of the file to the remote file on the WebDAV server. If the function succeeds, this means that the file was saved successfully.

This function does not flush encrypted files. If <i>hFile</i> is a handle to an encrypted file, <b>DavFlushFile</b> returns ERROR_SUCCESS without flushing the file data.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a>



<a href="https://msdn.microsoft.com/library/Aa364439(v=VS.85).aspx">FlushFileBuffers</a>



<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

