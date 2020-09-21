---
UID: NS:winsock2._WSANETWORKEVENTS
title: WSANETWORKEVENTS (winsock2.h)
description: The WSANETWORKEVENTS structure is used to store a socket's internal information about network events.
helpviewer_keywords: ["*LPWSANETWORKEVENTS","LPWSANETWORKEVENTS","LPWSANETWORKEVENTS structure pointer [Winsock]","WSANETWORKEVENTS","WSANETWORKEVENTS structure [Winsock]","_win32_wsanetworkevents_2","winsock.wsanetworkevents_2","winsock2/LPWSANETWORKEVENTS","winsock2/WSANETWORKEVENTS"]
old-location: winsock\wsanetworkevents_2.htm
tech.root: WinSock
ms.assetid: 72ae4aa8-4e15-4215-8dcb-45e394ac1313
ms.date: 12/05/2018
ms.keywords: '*LPWSANETWORKEVENTS, LPWSANETWORKEVENTS, LPWSANETWORKEVENTS structure pointer [Winsock], WSANETWORKEVENTS, WSANETWORKEVENTS structure [Winsock], _win32_wsanetworkevents_2, winsock.wsanetworkevents_2, winsock2/LPWSANETWORKEVENTS, winsock2/WSANETWORKEVENTS'
req.header: winsock2.h
req.include-header: 
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
req.typenames: WSANETWORKEVENTS, *LPWSANETWORKEVENTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSANETWORKEVENTS
 - winsock2/_WSANETWORKEVENTS
 - LPWSANETWORKEVENTS
 - winsock2/LPWSANETWORKEVENTS
 - WSANETWORKEVENTS
 - winsock2/WSANETWORKEVENTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSANETWORKEVENTS
---

# WSANETWORKEVENTS structure


## -description

The 
<b>WSANETWORKEVENTS</b> structure is used to store a socket's internal information about network events.

## -struct-fields

### -field lNetworkEvents

Indicates which of the FD_XXX network events have occurred.

### -field iErrorCode

Array that contains any associated error codes, with an array index that corresponds to the position of event bits in <b>lNetworkEvents</b>. The identifiers FD_READ_BIT, FD_WRITE_BIT and others can be used to index the <b>iErrorCode</b> array.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnetworkevents">WSAEnumNetworkEvents</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>