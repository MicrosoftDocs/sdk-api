---
UID: NF:netioapi.FreeMibTable
title: FreeMibTable function
author: windows-sdk-content
description: Frees the buffer allocated by the functions that return tables of network interfaces, addresses, and routes (GetIfTable2 and GetAnycastIpAddressTable, for example).
old-location: iphlp\freemibtable.htm
old-project: IpHlp
ms.assetid: 31c8cdc4-73c7-4e82-8226-c90320046199
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: FreeMibTable, FreeMibTable function [IP Helper], iphlp.freemibtable, netioapi/FreeMibTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# FreeMibTable function


## -description


The 
<b>FreeMibTable</b> function  frees the buffer allocated by the functions that return tables of network interfaces, addresses, and routes (<a href="https://msdn.microsoft.com/library/windows/hardware/ff552524">GetIfTable2</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff552508">GetAnycastIpAddressTable</a>, for example).


## -parameters




### -param Memory [in]

A pointer to the buffer to free.


## -returns



This function does not return a value.




## -remarks



The <b>FreeMibTable</b> function is defined on Windows Vista and later. 

The <b>FreeMibTable</b> function is used to free the internal buffers used by various functions to retrieve tables of interfaces, addresses, and routes. When these tables are no longer needed, then <b>FreeMibTable</b> should be called to release the memory used by these tables. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552508">GetAnycastIpAddressTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552521">GetIfStackTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552524">GetIfTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552531">GetInvertedIfStackTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552536">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552543">GetIpInterfaceTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552551">GetIpNetTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552559">GetIpPathTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552570">GetMulticastIpAddressTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552594">GetUnicastIpAddressTable</a>
 

 

