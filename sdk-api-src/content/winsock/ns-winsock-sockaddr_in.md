---
UID: NS:winsock.sockaddr_in
title: SOCKADDR_IN
author: windows-sdk-content
description: The sockaddr structure varies depending on the protocol selected.
old-location: winsock\sockaddr_2.htm
tech.root: winsock
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSOCKADDR_IN, *PSOCKADDR_IN, SOCKADDR, SOCKADDR_IN, SOCKADDR_IN6, _win32_sockaddr_2, sockaddr, sockaddr structure [Winsock], sockaddr_in, sockaddr_in6, sockaddr_in6_old, winsock.sockaddr_2, winsock/sockaddr"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winsock.h
req.include-header: 
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
product: Windows
targetos: Windows
req.typenames: SOCKADDR_IN, *PSOCKADDR_IN, *LPSOCKADDR_IN
req.redist: 
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




<a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a>
 

 

