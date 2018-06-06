---
UID: NF:iphlpapi.GetFriendlyIfIndex
title: GetFriendlyIfIndex function
author: windows-sdk-content
description: Takes an interface index and returns a backward-compatible interface index, that is, an index that uses only the lower 24 bits.
old-location: iphlp\getfriendlyifindex.htm
old-project: IpHlp
ms.assetid: 2c5b0b63-cbbb-4e89-be27-8e148a891542
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetFriendlyIfIndex, GetFriendlyIfIndex function [IP Helper], _iphlp_getfriendlyifindex, iphlp.getfriendlyifindex, iphlpapi/GetFriendlyIfIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iphlpapi.h
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetFriendlyIfIndex
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetFriendlyIfIndex function


## -description


The 
<b>GetFriendlyIfIndex</b> function takes an interface index and returns a backward-compatible interface index, that is, an index that uses only the lower 24 bits.


## -parameters




### -param IfIndex [in]

The interface index from which the backward-compatible or "friendly" interface index is derived.


## -returns



A backward-compatible interface index that uses only the lower 24 bits.




## -see-also




<a href="https://msdn.microsoft.com/bf16588d-3756-469e-afa2-e2e3dd537047">GetIfEntry</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a>
 

 

