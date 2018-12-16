---
UID: NS:winsock2.servent
title: SERVENT
author: windows-sdk-content
description: The servent structure is used to store or return the name and service number for a given service name.
old-location: winsock\servent_2.htm
tech.root: winsock
ms.assetid: 8696b854-4d37-4d1b-8383-169b5dc7a2ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSERVENT, *PSERVENT, FAR *LPSERVENT, FAR *LPSERVENT structure [Winsock], PSERVENT, PSERVENT structure pointer [Winsock], SERVENT, SERVENT structure [Winsock], _win32_servent_2, servent, servent structure [Winsock], winsock.servent_2, winsock/FAR *LPSERVENT, winsock/PSERVENT, winsock/servent"
ms.topic: struct
req.header: winsock2.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock.h
api_name:
 - SERVENT
product: Windows
targetos: Windows
req.typenames: SERVENT, *PSERVENT, *LPSERVENT
req.redist: 
---

# SERVENT structure


## -description


The 
<b>servent</b> structure is used to store or return the name and service number for a given service name.


## -struct-fields




### -field s_name

The official name of the service.


### -field s_aliases

A <b>NULL</b>-terminated array of alternate names.


### -field s_port

The port number at which the service can be contacted. Port numbers are returned in network byte order.


### -field s_proto

The name of the protocol to use when contacting the service.


## -see-also




<a href="https://msdn.microsoft.com/730fa372-f620-4d21-99b9-3e7b79932792">getservbyname</a>
 

 

