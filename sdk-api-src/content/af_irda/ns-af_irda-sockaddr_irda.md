---
UID: NS:af_irda._SOCKADDR_IRDA
title: SOCKADDR_IRDA (af_irda.h)
description: The SOCKADDR_IRDA structure is used in conjunction with IrDA socket operations, defined by address family AF_IRDA.
helpviewer_keywords: ["*LPSOCKADDR_IRDA","*PSOCKADDR_IRDA","LPSOCKADDR_IRDA","LPSOCKADDR_IRDA structure pointer [Winsock]","PSOCKADDR_IRDA","PSOCKADDR_IRDA structure pointer [Winsock]","SOCKADDR_IRDA","SOCKADDR_IRDA structure [Winsock]","_win32_sockaddr_irda_2","af_irda/LPSOCKADDR_IRDA","af_irda/PSOCKADDR_IRDA","af_irda/SOCKADDR_IRDA","winsock.sockaddr_irda_2"]
old-location: winsock\sockaddr_irda_2.htm
tech.root: WinSock
ms.assetid: 6a5b8d70-f005-4d84-b575-22ad48564793
ms.date: 12/05/2018
ms.keywords: '*LPSOCKADDR_IRDA, *PSOCKADDR_IRDA, LPSOCKADDR_IRDA, LPSOCKADDR_IRDA structure pointer [Winsock], PSOCKADDR_IRDA, PSOCKADDR_IRDA structure pointer [Winsock], SOCKADDR_IRDA, SOCKADDR_IRDA structure [Winsock], _win32_sockaddr_irda_2, af_irda/LPSOCKADDR_IRDA, af_irda/PSOCKADDR_IRDA, af_irda/SOCKADDR_IRDA, winsock.sockaddr_irda_2'
req.header: af_irda.h
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
req.typenames: SOCKADDR_IRDA, *PSOCKADDR_IRDA, *LPSOCKADDR_IRDA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOCKADDR_IRDA
 - af_irda/_SOCKADDR_IRDA
 - PSOCKADDR_IRDA
 - af_irda/PSOCKADDR_IRDA
 - SOCKADDR_IRDA
 - af_irda/SOCKADDR_IRDA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Af_irda.h
api_name:
 - SOCKADDR_IRDA
---

# SOCKADDR_IRDA structure


## -description

The 
<b>SOCKADDR_IRDA</b> structure is used in conjunction with IrDA socket operations, defined by address family AF_IRDA.

## -struct-fields

### -field irdaAddressFamily

Address family. This member is always AF_IRDA.

### -field irdaDeviceID

Device identifier (ID) of the IrDA device to which the client wants to issue the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> function call. Ignored by server applications.

### -field irdaServiceName

Well-known service name associated with a server application. Specified by servers during their 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function call.

## -remarks

Client applications make use of each field in the 
<b>SOCKADDR_IRDA</b> structure. The <b>irdaDeviceID</b> member is obtained by a previous discovery operation performed by making a 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>(IRLMP_ENUMDEVICES) function call. For more information on performing a discovery operation, see the Notes for IrDA Sockets section in the Remarks section of 
<b>getsockopt</b>.

The <b>irdaServiceName</b> member is filled with the well-known value that the server application specified in its 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function call.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>