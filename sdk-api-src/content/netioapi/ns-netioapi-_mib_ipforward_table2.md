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

# _MIB_IPFORWARD_TABLE2 structure


## -description


The 
<b>MIB_IPFORWARD_TABLE2</b> structure contains a table of IP route entries.



## -struct-fields




### -field NumEntries

A value that specifies the number of IP route entries in the array.


### -field Table

An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structures containing IP route entries.


## -remarks



The <b>MIB_IPFORWARD_TABLE2</b> structure is defined on Windows Vista and later. 

The <b>GetIpForwardTable2</b> function enumerates the IP route entries on a local system and returns this information in a <b>MIB_IPFORWARD_TABLE2</b> structure. 



The <b>GetIpForwardEntry2</b> function retrieves a single IP route entry and returns this information in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure.

The <b>MIB_IPFORWARD_TABLE2</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IPFORWARD_ROW2</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IPFORWARD_ROW2</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<b>GetIpForwardEntry2</b>



<b>GetIpForwardTable2</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a>
 

 

