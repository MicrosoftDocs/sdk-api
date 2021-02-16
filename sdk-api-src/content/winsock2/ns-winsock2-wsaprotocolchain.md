---
UID: NS:winsock2._WSAPROTOCOLCHAIN
title: WSAPROTOCOLCHAIN (winsock2.h)
description: The WSAPROTOCOLCHAIN structure contains a counted list of Catalog Entry identifiers that comprise a protocol chain.
helpviewer_keywords: ["*LPWSAPROTOCOLCHAIN","LPWSAPROTOCOLCHAIN","LPWSAPROTOCOLCHAIN structure pointer [Winsock]","WSAPROTOCOLCHAIN","WSAPROTOCOLCHAIN structure [Winsock]","_win32_wsaprotocolchain_2","winsock.wsaprotocolchain_2","winsock2/LPWSAPROTOCOLCHAIN","winsock2/WSAPROTOCOLCHAIN"]
old-location: winsock\wsaprotocolchain_2.htm
tech.root: WinSock
ms.assetid: c0676f45-e3e3-45f2-9b34-d7318fddc282
ms.date: 12/05/2018
ms.keywords: '*LPWSAPROTOCOLCHAIN, LPWSAPROTOCOLCHAIN, LPWSAPROTOCOLCHAIN structure pointer [Winsock], WSAPROTOCOLCHAIN, WSAPROTOCOLCHAIN structure [Winsock], _win32_wsaprotocolchain_2, winsock.wsaprotocolchain_2, winsock2/LPWSAPROTOCOLCHAIN, winsock2/WSAPROTOCOLCHAIN'
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
req.typenames: WSAPROTOCOLCHAIN, *LPWSAPROTOCOLCHAIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSAPROTOCOLCHAIN
 - winsock2/_WSAPROTOCOLCHAIN
 - LPWSAPROTOCOLCHAIN
 - winsock2/LPWSAPROTOCOLCHAIN
 - WSAPROTOCOLCHAIN
 - winsock2/WSAPROTOCOLCHAIN
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
 - WSAPROTOCOLCHAIN
---

# WSAPROTOCOLCHAIN structure


## -description

The 
<b>WSAPROTOCOLCHAIN</b> structure contains a counted list of Catalog Entry identifiers that comprise a protocol chain.

## -struct-fields

### -field ChainLen

Length of the chain, in bytes. The following settings apply: 




Setting <b>ChainLen</b> to zero indicates a layered protocol

Setting <b>ChainLen</b> to one indicates a base protocol

Setting <b>ChainLen</b> to greater than one indicates a protocol chain

### -field ChainEntries

Array of protocol chain entries.

## -remarks

If the length of the chain is larger than 1, this structure represents a protocol chain which consists of one or more layered protocols on top of a base protocol. The corresponding Catalog Entry IDs are in the ProtocolChain.ChainEntries array starting with the layered protocol at the top (the zeroth element in the ProtocolChain.ChainEntries array) and ending with the base protocol. Refer to Windows Sockets 2 Service Provider Interface for more information on protocol chains.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>