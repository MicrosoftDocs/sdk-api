---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

