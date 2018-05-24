---
UID: NF:netioapi.ConvertInterfaceLuidToIndex
title: ConvertInterfaceLuidToIndex function
author: windows-driver-content
description: Converts a locally unique identifier (LUID) for a network interface to the local index for the interface.
old-location: iphlp\convertinterfaceluidtoindex.htm
old-project: IpHlp
ms.assetid: 904cd94c-dd46-42ac-aef2-ffed4b3e5899
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ConvertInterfaceLuidToIndex, ConvertInterfaceLuidToIndex function [IP Helper], iphlp.convertinterfaceluidtoindex, netioapi/ConvertInterfaceLuidToIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	ConvertInterfaceLuidToIndex
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ConvertInterfaceLuidToIndex function


## -description


The 
<b>ConvertInterfaceLuidToIndex</b> function converts a locally unique identifier (LUID) for a network interface to the local index  for the interface.


## -parameters




### -param InterfaceLuid [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a> for a network interface.


### -param InterfaceIndex [out]

The local index  value for the interface.


## -returns



On success, 
<b>ConvertInterfaceLuidToIndex</b> returns NO_ERROR. Any nonzero return value indicates failure and a <b>NET_IFINDEX_UNSPECIFIED</b> is returned in the <i>InterfaceIndex</i> parameter. 

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>
								ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters was invalid. This error is returned if either the <i>InterfaceLuid</i> or <i>InterfaceIndex</i> parameter was <b>NULL</b> or if the <i>InterfaceLuid</i> parameter was invalid. 

</td>
</tr>
</table>
 




## -remarks



The <b>ConvertInterfaceLuidToIndex</b> function is available on Windows Vista
  
   and later.

The <b>ConvertInterfaceLuidToIndex</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546130">ConvertInterfaceAliasToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546137">ConvertInterfaceGuidToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546141">ConvertInterfaceIndexToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546151">ConvertInterfaceLuidToAlias</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546156">ConvertInterfaceLuidToGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546171">ConvertInterfaceLuidToNameA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546175">ConvertInterfaceLuidToNameW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546185">ConvertInterfaceNameToLuidA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546192">ConvertInterfaceNameToLuidW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553785">if_indextoname</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553788">if_nametoindex</a>
 

 

