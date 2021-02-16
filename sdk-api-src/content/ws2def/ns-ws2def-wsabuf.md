---
UID: NS:ws2def._WSABUF
title: WSABUF (ws2def.h)
description: The WSABUF structure enables the creation or manipulation of a data buffer used by some Winsock functions.
helpviewer_keywords: ["*LPWSABUF","LPWSABUF","LPWSABUF structure pointer [Winsock]","WSABUF","WSABUF structure [Winsock]","WSABUFA","_win32_wsabuf_2","winsock.wsabuf_2","ws2def/LPWSABUF","ws2def/WSABUF"]
old-location: winsock\wsabuf_2.htm
tech.root: WinSock
ms.assetid: a012c3ba-67fd-4fcf-84d1-85e9d495c29c
ms.date: 12/05/2018
ms.keywords: '*LPWSABUF, LPWSABUF, LPWSABUF structure pointer [Winsock], WSABUF, WSABUF structure [Winsock], WSABUFA, _win32_wsabuf_2, winsock.wsabuf_2, ws2def/LPWSABUF, ws2def/WSABUF'
req.header: ws2def.h
req.include-header: Winsock2.h
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
targetos: Windows
req.typenames: WSABUF, *LPWSABUF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSABUF
 - ws2def/_WSABUF
 - LPWSABUF
 - ws2def/LPWSABUF
 - WSABUF
 - ws2def/WSABUF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2def.h
api_name:
 - WSABUF
---

# WSABUF structure


## -description

The 
<b>WSABUF</b> structure enables the creation or manipulation of a data buffer used by some Winsock functions.

## -struct-fields

### -field len

The length of the buffer, in bytes.

### -field buf

A pointer to the buffer.

