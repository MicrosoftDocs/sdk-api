---
UID: NS:winsock2.servent
title: SERVENT (winsock2.h)
description: The SERVENT structure (winsock2.h) is used to store or return the name and service number for a given service name. 
helpviewer_keywords: ["*LPSERVENT","*PSERVENT","FAR *LPSERVENT","FAR *LPSERVENT structure [Winsock]","PSERVENT","PSERVENT structure pointer [Winsock]","SERVENT","SERVENT structure [Winsock]","_win32_servent_2","servent","servent structure [Winsock]","winsock.servent_2","winsock/FAR *LPSERVENT","winsock/PSERVENT","winsock/servent"]
old-location: winsock\servent_2.htm
tech.root: WinSock
ms.assetid: 8696b854-4d37-4d1b-8383-169b5dc7a2ae
ms.date: 08/03/2022
ms.keywords: '*LPSERVENT, *PSERVENT, FAR *LPSERVENT, FAR *LPSERVENT structure [Winsock], PSERVENT, PSERVENT structure pointer [Winsock], SERVENT, SERVENT structure [Winsock], _win32_servent_2, servent, servent structure [Winsock], winsock.servent_2, winsock/FAR *LPSERVENT, winsock/PSERVENT, winsock/servent'
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
targetos: Windows
req.typenames: SERVENT, *PSERVENT, *LPSERVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - servent
 - winsock2/servent
 - PSERVENT
 - winsock2/PSERVENT
 - SERVENT
 - winsock2/SERVENT
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
 - SERVENT
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

<a href="/windows/desktop/api/winsock/nf-winsock-getservbyname">getservbyname</a>
