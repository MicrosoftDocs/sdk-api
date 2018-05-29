---
UID: NS:winsock2.protoent
title: protoent
author: windows-sdk-content
description: The protoent structure contains the name and protocol numbers that correspond to a given protocol name.
old-location: winsock\protoent_2.htm
old-project: WinSock
ms.assetid: 8fc729dd-5a73-42a1-9c3f-adc68d83d863
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: "*LPPROTOENT, *PPROTOENT, PROTOENT, _win32_protoent_2, protoent, protoent structure [Winsock], winsock.protoent_2, winsock/protoent"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: PROTOENT, *PPROTOENT, *LPPROTOENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winsock.h
api_name:
-	protoent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# protoent structure


## -description



			The <b>protoent</b> structure contains the name and protocol numbers that correspond to a given protocol name. Applications must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, and therefore, the application should copy any information it needs before issuing any other Windows Sockets function calls.


## -struct-fields




### -field p_name

Official name of the protocol.


### -field p_aliases

Null-terminated array of alternate names.


### -field p_proto

Protocol number, in host byte order.

