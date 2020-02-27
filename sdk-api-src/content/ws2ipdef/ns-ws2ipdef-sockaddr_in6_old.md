---
UID: NS:ws2ipdef.sockaddr_in6_old
title: sockaddr_in6_old (ws2ipdef.h)
description: The sockaddr structure varies depending on the protocol selected.
old-location: winsock\sockaddr_2.htm
tech.root: WinSock
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
ms.date: 12/05/2018
ms.keywords: SOCKADDR, SOCKADDR_IN, SOCKADDR_IN6, _win32_sockaddr_2, sockaddr, sockaddr structure [Winsock], sockaddr_in, sockaddr_in6, sockaddr_in6_old, winsock.sockaddr_2, winsock/sockaddr
f1_keywords:
- ws2ipdef/sockaddr
dev_langs:
- c++
req.header: ws2ipdef.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# sockaddr_in6_old structure


## -description


The 
sockaddr structure varies depending on the protocol selected. Except for the <i>sin*_family</i> parameter, 
sockaddr contents are expressed in network byte order.


## -struct-fields




### -field sin6_family

 


### -field sin6_port

 


### -field sin6_flowinfo

 


### -field sin6_addr

 




#### - sa_data


#### - sa_family


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a>
 

 

