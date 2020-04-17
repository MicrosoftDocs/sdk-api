---
UID: NS:winsock.sockaddr
title: SOCKADDR (winsock.h)
description: The sockaddr structure varies depending on the protocol selected.helpviewer_keywords: ["*LPSOCKADDR","*PSOCKADDR","SOCKADDR","SOCKADDR_IN","SOCKADDR_IN6","_win32_sockaddr_2","sockaddr","sockaddr structure [Winsock]","sockaddr_in","sockaddr_in6","sockaddr_in6_old","winsock.sockaddr_2","winsock/sockaddr"]
old-location: winsock\sockaddr_2.htm
tech.root: WinSock
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
ms.date: 12/05/2018
ms.keywords: '*LPSOCKADDR, *PSOCKADDR, SOCKADDR, SOCKADDR_IN, SOCKADDR_IN6, _win32_sockaddr_2, sockaddr, sockaddr structure [Winsock], sockaddr_in, sockaddr_in6, sockaddr_in6_old, winsock.sockaddr_2, winsock/sockaddr'
f1_keywords:
- winsock/sockaddr
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- winsock.h
api_name:
- sockaddr
targetos: Windows
req.typenames: SOCKADDR, *PSOCKADDR, *LPSOCKADDR
req.redist: 
ms.custom: 19H1
---

# SOCKADDR structure


## -description


The 
sockaddr structure varies depending on the protocol selected. Except for the <i>sin*_family</i> parameter, 
sockaddr contents are expressed in network byte order.


## -struct-fields




### -field sa_family


### -field sa_data


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a>
 

 

