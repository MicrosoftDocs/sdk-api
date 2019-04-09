---
UID: NF:netioapi.FreeMibTable
title: FreeMibTable function (netioapi.h)
author: windows-sdk-content
description: Frees the buffer allocated by the functions that return tables of network interfaces, addresses, and routes (GetIfTable2 and GetAnycastIpAddressTable, for example).
old-location: iphlp\freemibtable.htm
tech.root: IpHlp
ms.assetid: 31c8cdc4-73c7-4e82-8226-c90320046199
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeMibTable, FreeMibTable function [IP Helper], iphlp.freemibtable, netioapi/FreeMibTable
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - FreeMibTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeMibTable function


## -description


The 
<b>FreeMibTable</b> function  frees the buffer allocated by the functions that return tables of network interfaces, addresses, and routes (<a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a> and <a href="https://msdn.microsoft.com/4eccae59-00be-4f9c-bb62-a507d7dad2e0">GetAnycastIpAddressTable</a>, for example).


## -parameters




### -param Memory [in]

A pointer to the buffer to free.


## -returns



This function does not return a value.




## -remarks



The <b>FreeMibTable</b> function is defined on Windows Vista and later. 

The <b>FreeMibTable</b> function is used to free the internal buffers used by various functions to retrieve tables of interfaces, addresses, and routes. When these tables are no longer needed, then <b>FreeMibTable</b> should be called to release the memory used by these tables. 




## -see-also




<a href="https://msdn.microsoft.com/4eccae59-00be-4f9c-bb62-a507d7dad2e0">GetAnycastIpAddressTable</a>



<a href="https://msdn.microsoft.com/c1b0f091-2aef-447e-9866-a886838a6267">GetIfStackTable</a>



<a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a>



<a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/d1808ded-2798-46cc-8021-fdbcd3da60ea">GetInvertedIfStackTable</a>



<a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/09f2bbff-3281-41ae-878f-61c5afa20ec5">GetIpInterfaceTable</a>



<a href="https://msdn.microsoft.com/6c45d735-9a07-41ca-8d8a-919f32c98a3c">GetIpNetTable2</a>



<a href="https://msdn.microsoft.com/e03816a4-0b86-4e0b-a45e-8148c8ba5472">GetIpPathTable</a>



<a href="https://msdn.microsoft.com/0958e92e-12ed-42e0-aa04-b8c4544f6642">GetMulticastIpAddressTable</a>



<a href="https://msdn.microsoft.com/bdafc4a4-5f3c-4dd5-ba9b-4f6045a82652">GetUnicastIpAddressTable</a>
 

 

