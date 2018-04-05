---
UID: NF:netioapi.ConvertInterfaceAliasToLuid
title: ConvertInterfaceAliasToLuid function
author: windows-driver-content
description: Converts an interface alias name for a network interface to the locally unique identifier (LUID) for the interface.
old-location: iphlp\convertinterfacealiastoluid.htm
old-project: IpHlp
ms.assetid: 7fa80938-d475-4ace-b463-a53aac26e88b
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: ConvertInterfaceAliasToLuid, ConvertInterfaceAliasToLuid function [IP Helper], iphlp.convertinterfacealiastoluid, netioapi/ConvertInterfaceAliasToLuid
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
-	ConvertInterfaceAliasToLuid
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ConvertInterfaceAliasToLuid function


## -description


The 
<b>ConvertInterfaceAliasToLuid</b> function converts an interface alias name for a network interface to the locally unique identifier (LUID) for the interface.


## -parameters




### -param InterfaceAlias [in]

A pointer to a <b>NULL</b>-terminated Unicode string containing the alias name of the network interface.


### -param InterfaceLuid [out]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a> for this interface.


## -returns



On success, 
<b>ConvertInterfaceAliasToLuid</b> returns NO_ERROR. Any nonzero return value indicates failure and a <b>NULL</b> is returned in the <i>InterfaceLuid</i> parameter. 

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
One of the parameters was invalid. This error is returned if either the <i>InterfaceAlias</i> or <i>InterfaceLuid</i> parameter was <b>NULL</b> or if the <i>InterfaceAlias</i> parameter was invalid.

</td>
</tr>
</table>
 




## -remarks



The <b>ConvertInterfaceAliasToLuid</b> function is available on Windows Vista
  
   and later.

The <b>ConvertInterfaceAliasToLuid</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546137">ConvertInterfaceGuidToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546141">ConvertInterfaceIndexToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546151">ConvertInterfaceLuidToAlias</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546156">ConvertInterfaceLuidToGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546167">ConvertInterfaceLuidToIndex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546171">ConvertInterfaceLuidToNameA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546175">ConvertInterfaceLuidToNameW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546185">ConvertInterfaceNameToLuidA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546192">ConvertInterfaceNameToLuidW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553785">if_indextoname</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553788">if_nametoindex</a>
 

 

