---
UID: NS:winsock2._AFPROTOCOLS
title: "_AFPROTOCOLS"
author: windows-sdk-content
description: The AFPROTOCOLS structure supplies a list of protocols to which application programmers can constrain queries. The AFPROTOCOLS structure is used for query purposes only.
old-location: winsock\afprotocols_2.htm
old-project: winsock
ms.assetid: ffd43aa1-bbc4-46f1-ad77-26c48f9ac0b7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPAFPROTOCOLS, *PAFPROTOCOLS, AFPROTOCOLS, AFPROTOCOLS structure [Winsock], LPAFPROTOCOLS, LPAFPROTOCOLS structure pointer [Winsock], PAFPROTOCOLS, PAFPROTOCOLS structure pointer [Winsock], _AFPROTOCOLS, _win32_afprotocols_2, winsock.afprotocols_2, winsock2/AFPROTOCOLS, winsock2/LPAFPROTOCOLS, winsock2/PAFPROTOCOLS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: AFPROTOCOLS, *PAFPROTOCOLS, *LPAFPROTOCOLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - AFPROTOCOLS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _AFPROTOCOLS structure


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




<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>



<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>



<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQuerySet</a>
 

 

