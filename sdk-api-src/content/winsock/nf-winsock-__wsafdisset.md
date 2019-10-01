---
UID: NF:winsock.__WSAFDIsSet
title: __WSAFDIsSet function (winsock.h)
author: windows-sdk-content
description: The __WSAFDIsSet function specifies whether a socket is included in a set of socket descriptors.
old-location: winsock\wsafdisset.htm
tech.root: WinSock
ms.assetid: ca420136-0b3b-45a1-85ce-83ab6ba1a70a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "__WSAFDIsSet, __WSAFDIsSet function [Winsock], winsock.wsafdisset, winsock/__WSAFDIsSet"
ms.topic: function
f1_keywords: 
 - "winsock/__WSAFDIsSet"
req.header: winsock.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - __WSAFDIsSet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# __WSAFDIsSet function


## -description


The <b>__WSAFDIsSet</b> function specifies whether a socket is included in a set of socket descriptors.


## -parameters




### -param arg1

TBD


### -param arg2

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-fd_set">fd_set</a> structure containing the set of socket descriptors. The <b>__WSAFDIsSet</b> function determines whether the socket specified in the <i>fd</i> parameter is a member of that set.


#### - fd

Descriptor identifying a socket.


## -remarks



<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-fd_set">fd_set</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-select">select</a>
 

 

