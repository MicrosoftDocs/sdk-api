---
UID: NS:ws2def.sockaddr
title: sockaddr
author: windows-sdk-content
description: The SOCKADDR structure is a generic structure that specifies a transport address.
old-location: netvista\sockaddr.htm
old-project: netvista
ms.assetid: af5ad9ae-3987-4f16-a8a6-14e3e3d0fa6a
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*LPSOCKADDR, *PSOCKADDR, PSOCKADDR, PSOCKADDR structure pointer [Network Drivers Starting with Windows Vista], SOCKADDR, SOCKADDR structure [Network Drivers Starting with Windows Vista], netvista.sockaddr, sockaddr, ws2def/PSOCKADDR, ws2def/SOCKADDR, wskref_4198a308-7f9c-4c7c-ba32-8f11e65e2349.xml"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: Wsk.h
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ws2def.h
api_name:
-	SOCKADDR
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
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff571151">WSK Address Families</a>.


### -field sa_data

An array of 14 bytes that contains the transport address data.


## -remarks



The SOCKADDR structure is large enough to contain a transport address for most address families. For a
    structure that is guaranteed to be large enough to contain a transport address for all possible address
    families, see 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a>.

A WSK application typically does not access the 
    <b>sa_data</b> member directly. Instead, a pointer to a SOCKADDR structure is normally cast to a pointer
    to the specific SOCKADDR structure type that corresponds to a particular address family.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571164">WSK_DATAGRAM_INDICATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571109">WskAccept</a>



<a href="https://msdn.microsoft.com/672440f0-810a-4e68-82a5-d038770898c5">WskAcceptEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571121">WskBind</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571125">WskConnect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571133">WskGetLocalAddress</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571135">WskGetRemoteAddress</a>



<a href="https://msdn.microsoft.com/40f184ac-4ef3-485a-a529-71c1f2716427">WskInspectEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571141">WskReceiveFrom</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571148">WskSendTo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571150">WskSocketConnect</a>
 

 

