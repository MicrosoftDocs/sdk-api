---
UID: NS:ws2def.sockaddr
title: sockaddr
author: windows-sdk-content
description: The SOCKADDR structure is a generic structure that specifies a transport address.
old-location: netvista\sockaddr.htm
old-project: netvista
ms.assetid: af5ad9ae-3987-4f16-a8a6-14e3e3d0fa6a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*LPSOCKADDR, *PSOCKADDR, PSOCKADDR, PSOCKADDR structure pointer [Network Drivers Starting with Windows Vista], SOCKADDR, SOCKADDR structure [Network Drivers Starting with Windows Vista], netvista.sockaddr, sockaddr, ws2def/PSOCKADDR, ws2def/SOCKADDR, wskref_4198a308-7f9c-4c7c-ba32-8f11e65e2349.xml"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: Wsk.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SOCKADDR, *PSOCKADDR, *LPSOCKADDR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2def.h
api_name:
 - SOCKADDR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# sockaddr structure


## -description


The SOCKADDR structure is a generic structure that specifies a transport address.


## -struct-fields




### -field sa_family

The address family for the transport address. For more information about supported address
     families, see 
     <a href="https://msdn.microsoft.com/library/Ff571151(v=VS.85).aspx">WSK Address Families</a>.


### -field sa_data

An array of 14 bytes that contains the transport address data.


## -remarks



The SOCKADDR structure is large enough to contain a transport address for most address families. For a
    structure that is guaranteed to be large enough to contain a transport address for all possible address
    families, see 
    <a href="https://msdn.microsoft.com/27e56c1a-ce11-4cdb-9be8-25ed2f94fb37">SOCKADDR_STORAGE</a>.

A WSK application typically does not access the 
    <b>sa_data</b> member directly. Instead, a pointer to a SOCKADDR structure is normally cast to a pointer
    to the specific SOCKADDR structure type that corresponds to a particular address family.




## -see-also




<a href="https://msdn.microsoft.com/27e56c1a-ce11-4cdb-9be8-25ed2f94fb37">SOCKADDR_STORAGE</a>



<a href="https://msdn.microsoft.com/061db3ca-80ed-419e-8cca-f49d1498b780">WSK_DATAGRAM_INDICATION</a>



<a href="https://msdn.microsoft.com/9fa8bb07-7ee5-400b-aaca-33db3911d79f">WskAccept</a>



<a href="https://msdn.microsoft.com/672440f0-810a-4e68-82a5-d038770898c5">WskAcceptEvent</a>



<a href="https://msdn.microsoft.com/520b02d0-a078-4af9-93a3-4fee5bbfee99">WskBind</a>



<a href="https://msdn.microsoft.com/66942ba4-40f9-4fdc-97f3-859309cd870d">WskConnect</a>



<a href="https://msdn.microsoft.com/13cd4199-63f8-49f3-a12f-86e1d367b4aa">WskGetLocalAddress</a>



<a href="https://msdn.microsoft.com/a2d65d55-744b-4851-b1fa-7087e0f06452">WskGetRemoteAddress</a>



<a href="https://msdn.microsoft.com/40f184ac-4ef3-485a-a529-71c1f2716427">WskInspectEvent</a>



<a href="https://msdn.microsoft.com/769fea0d-e35a-4385-8027-f1518c25b637">WskReceiveFrom</a>



<a href="https://msdn.microsoft.com/34257ef2-947a-463a-b234-04fbaffa9344">WskSendTo</a>



<a href="https://msdn.microsoft.com/b1482160-49db-4490-b347-ff9396abf2ff">WskSocketConnect</a>
 

 

