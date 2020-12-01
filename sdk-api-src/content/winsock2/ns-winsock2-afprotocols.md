---
UID: NS:winsock2._AFPROTOCOLS
title: AFPROTOCOLS (winsock2.h)
description: The AFPROTOCOLS structure supplies a list of protocols to which application programmers can constrain queries. The AFPROTOCOLS structure is used for query purposes only.
helpviewer_keywords: ["*LPAFPROTOCOLS","*PAFPROTOCOLS","AFPROTOCOLS","AFPROTOCOLS structure [Winsock]","LPAFPROTOCOLS","LPAFPROTOCOLS structure pointer [Winsock]","PAFPROTOCOLS","PAFPROTOCOLS structure pointer [Winsock]","_win32_afprotocols_2","winsock.afprotocols_2","winsock2/AFPROTOCOLS","winsock2/LPAFPROTOCOLS","winsock2/PAFPROTOCOLS"]
old-location: winsock\afprotocols_2.htm
tech.root: WinSock
ms.assetid: ffd43aa1-bbc4-46f1-ad77-26c48f9ac0b7
ms.date: 12/05/2018
ms.keywords: '*LPAFPROTOCOLS, *PAFPROTOCOLS, AFPROTOCOLS, AFPROTOCOLS structure [Winsock], LPAFPROTOCOLS, LPAFPROTOCOLS structure pointer [Winsock], PAFPROTOCOLS, PAFPROTOCOLS structure pointer [Winsock], _win32_afprotocols_2, winsock.afprotocols_2, winsock2/AFPROTOCOLS, winsock2/LPAFPROTOCOLS, winsock2/PAFPROTOCOLS'
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
req.typenames: AFPROTOCOLS, *PAFPROTOCOLS, *LPAFPROTOCOLS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AFPROTOCOLS
 - winsock2/_AFPROTOCOLS
 - PAFPROTOCOLS
 - winsock2/PAFPROTOCOLS
 - AFPROTOCOLS
 - winsock2/AFPROTOCOLS
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
 - AFPROTOCOLS
---

# AFPROTOCOLS structure


## -description

The 
<b>AFPROTOCOLS</b> structure supplies a list of protocols to which application programmers can constrain queries. The 
<b>AFPROTOCOLS</b> structure is used for query purposes only.

## -struct-fields

### -field iAddressFamily

Address family to which the query is to be constrained.

### -field iProtocol

Protocol to which the query is to be constrained.

## -remarks

The members of the 
<b>AFPROTOCOLS</b> structure are a functional pair, and only have meaning when used together, as protocol values have meaning only within the context of an address family.

## -see-also

<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQuerySet</a>