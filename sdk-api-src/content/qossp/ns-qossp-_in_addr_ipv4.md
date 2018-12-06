---
UID: NS:qossp._IN_ADDR_IPV4
title: "_IN_ADDR_IPV4"
author: windows-sdk-content
description: The IN_ADDR_IPV4 union stores an IPv4 address for use with RSVP FILTERSPECs.
old-location: qos\in_addr_ipv4.htm
tech.root: QOS
ms.assetid: 7e10cc9c-7ed4-449d-aeb9-21e3d75d0224
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPIN_ADDR_IPV4, *LPIN_ADDR_IPV4 union [QOS], IN_ADDR_IPV4, IN_ADDR_IPV4 union [QOS], _IN_ADDR_IPV4, qos.in_addr_ipv4, qossp/*LPIN_ADDR_IPV4, qossp/IN_ADDR_IPV4"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: qossp.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - IN_ADDR_IPV4
product: Windows
targetos: Windows
req.typenames: IN_ADDR_IPV4, *LPIN_ADDR_IPV4
req.redist: 
---

# _IN_ADDR_IPV4 structure


## -description


The <b>IN_ADDR_IPV4</b> union stores an IPv4 address for use with RSVP FILTERSPECs.


## -struct-fields




### -field Addr

IPv4 address, expressed as a ULONG.


### -field AddrBytes

IPv4 address, expressed as four UCHARs.


## -remarks



When working with IPv6 addresses, use <a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a>.




## -see-also




<a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a>
 

 

