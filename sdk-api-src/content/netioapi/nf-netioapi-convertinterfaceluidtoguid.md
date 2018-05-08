---
UID: NF:netioapi.ConvertInterfaceLuidToGuid
title: ConvertInterfaceLuidToGuid function
author: windows-driver-content
description: Converts a locally unique identifier (LUID) for a network interface to a globally unique identifier (GUID) for the interface.
old-location: iphlp\convertinterfaceluidtoguid.htm
old-project: IpHlp
ms.assetid: 9d5bd1e9-0bf1-405a-8726-8e2c9ba4e022
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ConvertInterfaceLuidToGuid, ConvertInterfaceLuidToGuid function [IP Helper], iphlp.convertinterfaceluidtoguid, netioapi/ConvertInterfaceLuidToGuid
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
-	ConvertInterfaceLuidToGuid
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ConvertInterfaceLuidToGuid function


## -description


The 
<b>ConvertInterfaceLuidToGuid</b> function converts a locally unique identifier (LUID) for a network interface to a globally unique identifier (GUID) for the interface.


## -parameters




### -param InterfaceLuid [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a> for a network interface.


### -param InterfaceGuid [out]

A pointer to the <b>GUID</b> for this interface.


## -returns



On success, 
<b>ConvertInterfaceLuidToGuid</b> returns NO_ERROR. Any nonzero return value indicates failure and a <b>NULL</b> is returned in the <i>InterfaceGuid</i> parameter. 

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters was invalid. This error is returned if either the <i>InterfaceLuid</i> or <i>InterfaceGuid</i> parameter was <b>NULL</b> or if the <i>InterfaceLuid</i> parameter was invalid.

</td>
</tr>
</table>
 




## -remarks



The <b>ConvertInterfaceLuidToGuid</b> function is available on Windows Vista
  
   and later.

The <b>ConvertInterfaceLuidToGuid</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546130">ConvertInterfaceAliasToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546137">ConvertInterfaceGuidToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546141">ConvertInterfaceIndexToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546151">ConvertInterfaceLuidToAlias</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546167">ConvertInterfaceLuidToIndex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546171">ConvertInterfaceLuidToNameA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546175">ConvertInterfaceLuidToNameW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546185">ConvertInterfaceNameToLuidA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546192">ConvertInterfaceNameToLuidW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553785">if_indextoname</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553788">if_nametoindex</a>
 

 

