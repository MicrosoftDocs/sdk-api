---
UID: NS:winsock.sockaddr_in
title: SOCKADDR_IN (winsock.h)
description: The SOCKADDR_IN (winsock.h) structure varies depending on the protocol selected.
helpviewer_keywords: ["*LPSOCKADDR_IN","*PSOCKADDR_IN","SOCKADDR","SOCKADDR_IN","SOCKADDR_IN6","_win32_sockaddr_2","sockaddr","sockaddr structure [Winsock]","sockaddr_in","sockaddr_in6","sockaddr_in6_old","winsock.sockaddr_2","winsock/sockaddr"]
old-location: winsock\sockaddr_2.htm
tech.root: WinSock
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
ms.date: 08/16/2022
ms.keywords: '*LPSOCKADDR_IN, *PSOCKADDR_IN, SOCKADDR, SOCKADDR_IN, SOCKADDR_IN6, _win32_sockaddr_2, sockaddr, sockaddr structure [Winsock], sockaddr_in, sockaddr_in6, sockaddr_in6_old, winsock.sockaddr_2, winsock/sockaddr'
req.header: winsock.h
req.include-header: Ws2ipdef.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SOCKADDR_IN, *PSOCKADDR_IN, *LPSOCKADDR_IN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - sockaddr_in
 - winsock/sockaddr_in
 - PSOCKADDR_IN
 - winsock/PSOCKADDR_IN
 - SOCKADDR_IN
 - winsock/SOCKADDR_IN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock.h
api_name:
 - sockaddr
---

# SOCKADDR_IN structure


## -description

The 
sockaddr structure varies depending on the protocol selected. Except for the <i>sin*_family</i> parameter, 
sockaddr contents are expressed in network byte order.

## -struct-fields

### -field sin_family

### -field sin_port

### -field sin_addr

### -field sin_zero

 




#### - sa_data


#### - sa_family

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a>
