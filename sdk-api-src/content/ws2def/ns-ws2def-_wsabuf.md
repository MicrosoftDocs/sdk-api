---
UID: NS:ws2def._WSABUF
title: "_WSABUF"
author: windows-sdk-content
description: The WSABUF structure enables the creation or manipulation of a data buffer used by some Winsock functions.
old-location: winsock\wsabuf_2.htm
old-project: WinSock
ms.assetid: a012c3ba-67fd-4fcf-84d1-85e9d495c29c
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: "*LPWSABUF, LPWSABUF, LPWSABUF structure pointer [Winsock], WSABUF, WSABUF structure [Winsock], WSABUFA, _WSABUF, _win32_wsabuf_2, winsock.wsabuf_2, ws2def/LPWSABUF, ws2def/WSABUF"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSABUF, *LPWSABUF
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2def.h
api_name:
 - WSABUF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSABUF structure


## -description



			The 
<b>WSABUF</b> structure enables the creation or manipulation of a data buffer used by some Winsock functions.


## -struct-fields




### -field len

The length of the buffer, in bytes.


### -field buf

A pointer to the buffer.

