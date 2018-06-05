---
UID: NF:winsock.__WSAFDIsSet
title: "__WSAFDIsSet function"
author: windows-sdk-content
description: The __WSAFDIsSet function specifies whether a socket is included in a set of socket descriptors.
old-location: winsock\wsafdisset.htm
old-project: WinSock
ms.assetid: ca420136-0b3b-45a1-85ce-83ab6ba1a70a
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: "__WSAFDIsSet, __WSAFDIsSet function [Winsock], winsock.wsafdisset, winsock/__WSAFDIsSet"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: smiVENDORINFO, *smiLPVENDORINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ws2_32.dll
api_name:
-	__WSAFDIsSet
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# __WSAFDIsSet function


## -description


The <b>__WSAFDIsSet</b> function specifies whether a socket is included in a set of socket descriptors.


## -parameters




### -param

TBD




#### - fd

Descriptor identifying a socket.


#### - set

Pointer to an <a href="https://msdn.microsoft.com/2af5d69d-190e-4814-8d8b-438431808625">fd_set</a> structure containing the set of socket descriptors. The <b>__WSAFDIsSet</b> function determines whether the socket specified in the <i>fd</i> parameter is a member of that set.


## -remarks



<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/2af5d69d-190e-4814-8d8b-438431808625">fd_set</a>



<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>
 

 

