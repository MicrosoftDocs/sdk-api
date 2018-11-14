---
UID: NF:winsock2.FD_SET
title: FD_SET macro
author: windows-sdk-content
description: Fd_set structure is used by Windows Sockets (Winsock) functions and service providers to place sockets into a set.
old-location: winsock\fd_set_2.htm
tech.root: winsock
ms.assetid: 2af5d69d-190e-4814-8d8b-438431808625
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FD_SET, _win32_fd_set_2, fd_set, fd_set structure [Winsock], winsock.fd_set_2, winsock/fd_set
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winsock2.h
req.include-header: Winsock2.h, Winsock.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock.h
api_name:
 - fd_set
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- winsock2.h
: 
- FD_SET
: 
---

# FD_SET macro


## -description


The 
<b>fd_set</b> structure is used by various Windows Sockets functions and service providers, such as the 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> function, to place sockets into a "set" for various purposes, such as testing a given socket for readability using the <i>readfds</i> parameter of the 
<b>select</b> function.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>
 

 

