---
UID: NS:af_irda._SOCKADDR_IRDA
title: "_SOCKADDR_IRDA"
author: windows-sdk-content
description: The SOCKADDR_IRDA structure is used in conjunction with IrDA socket operations, defined by address family AF_IRDA.
old-location: winsock\sockaddr_irda_2.htm
old-project: WinSock
ms.assetid: 6a5b8d70-f005-4d84-b575-22ad48564793
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*LPSOCKADDR_IRDA, *PSOCKADDR_IRDA, LPSOCKADDR_IRDA, LPSOCKADDR_IRDA structure pointer [Winsock], PSOCKADDR_IRDA, PSOCKADDR_IRDA structure pointer [Winsock], SOCKADDR_IRDA, SOCKADDR_IRDA structure [Winsock], _SOCKADDR_IRDA, _win32_sockaddr_irda_2, af_irda/LPSOCKADDR_IRDA, af_irda/PSOCKADDR_IRDA, af_irda/SOCKADDR_IRDA, winsock.sockaddr_irda_2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SOCKADDR_IRDA, *PSOCKADDR_IRDA, *LPSOCKADDR_IRDA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Af_irda.h
api_name:
 - SOCKADDR_IRDA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _SOCKADDR_IRDA structure


## -description



			The 
<b>SOCKADDR_IRDA</b> structure is used in conjunction with IrDA socket operations, defined by address family AF_IRDA.


## -struct-fields




### -field irdaAddressFamily

Address family. This member is always AF_IRDA.


### -field irdaDeviceID

Device identifier (ID) of the IrDA device to which the client wants to issue the 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> function call. Ignored by server applications.


### -field irdaServiceName

Well-known service name associated with a server application. Specified by servers during their 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function call.


## -remarks



Client applications make use of each field in the 
<b>SOCKADDR_IRDA</b> structure. The <b>irdaDeviceID</b> member is obtained by a previous discovery operation performed by making a 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>(IRLMP_ENUMDEVICES) function call. For more information on performing a discovery operation, see the Notes for IrDA Sockets section in the Remarks section of 
<b>getsockopt</b>.

The <b>irdaServiceName</b> member is filled with the well-known value that the server application specified in its 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function call.




## -see-also




<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>



<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a>
 

 

