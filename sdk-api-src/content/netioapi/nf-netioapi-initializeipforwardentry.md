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

# InitializeIpForwardEntry function


## -description


The 
<b>InitializeIpForwardEntry</b> function  initializes a  <b>MIB_IPFORWARD_ROW2</b> structure with default values for an IP route entry on the local computer.  


## -parameters




### -param Row [out]

On entry, a pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure entry for an IP route entry. On return, the  <b>MIB_IPFORWARD_ROW2</b> structure pointed to by this parameter is initialized with default values for an IP route entry.


## -returns



This function does not return a value.




## -remarks



The <b>InitializeIpForwardEntry</b> function is defined on Windows Vista and later. 

The <b>InitializeIpForwardEntry</b> function must be used to initialize the members of a
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure entry with default values for an IP route entry for later use with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546209">CreateIpForwardEntry2</a> function.  

On input, <b>InitializeIpForwardEntry</b> must be passed a new <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure to initialize. 

On output, the <b>ValidLifetime</b> and <b>PreferredLifetime</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure pointed to by <i>Row</i> parameter will be initialized to infinite and the <b>Loopback</b>,  <b>AutoconfigureAddress</b>, <b>Publish</b>, and <b>Immortal</b> members  will be initialized to <b>TRUE</b>. In addition, the <b>SitePrefixLength</b>,   <b>Metric</b>, and  <b>Protocol</b> members are set to an illegal value and other fields are initialized to zero. 

After calling <b>InitializeIpForwardEntry</b>, an application can then change the
    members in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> entry it wishes to modify, and then call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546209">CreateIpForwardEntry2</a>  to add the new IP route entry to the local computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546209">CreateIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546365">DeleteIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552511">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552535">GetIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552536">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559252">MIB_IPFORWARD_TABLE2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568806">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570773">SetIpForwardEntry2</a>
 

 

