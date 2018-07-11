---
UID: NF:netioapi.ConvertInterfaceLuidToAlias
title: ConvertInterfaceLuidToAlias function
author: windows-sdk-content
description: Converts a locally unique identifier (LUID) for a network interface to an interface alias.
old-location: iphlp\convertinterfaceluidtoalias.htm
old-project: iphlp
ms.assetid: 86a821c1-e04b-4bc3-846d-767c55008aed
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: ConvertInterfaceLuidToAlias, ConvertInterfaceLuidToAlias function [IP Helper], iphlp.convertinterfaceluidtoalias, netioapi/ConvertInterfaceLuidToAlias
ms.prod: windows
ms.technology: windows-sdk
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
 - ConvertInterfaceLuidToAlias
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ConvertInterfaceLuidToAlias function


## -description


The 
<b>ConvertInterfaceLuidToAlias</b> function converts a locally unique identifier (LUID) for a network interface to an interface alias.


## -parameters




### -param InterfaceLuid [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a> for a network interface.


### -param InterfaceAlias [out]

A pointer to a buffer to hold the <b>NULL</b>-terminated Unicode string containing the alias name of the network interface when the function returns successfully.


### -param Length [in]

The length, in characters, of the buffer pointed to by the <i>InterfaceAlias</i> parameter. This value must be large enough to accommodate the alias name of the network interface and the terminating <b>NULL</b> character.  The maximum required length is
        <b>NDIS_IF_MAX_STRING_SIZE</b> + 1.


## -returns



On success, 
<b>ConvertInterfaceLuidToAlias</b> returns NO_ERROR. Any nonzero return value indicates failure. 

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
One of the parameters was invalid. This error is returned if either the <i>InterfaceLuid</i> or <i>InterfaceAlias</i> parameter was <b>NULL</b> or if the <i>InterfaceLuid</i> parameter was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command. This error is returned if the size of the buffer pointed to by the <i>InterfaceAlias</i> parameter was not large enough as specified in the <i>Length</i> parameter to hold the alias name.

</td>
</tr>
</table>
 




## -remarks



The <b>ConvertInterfaceLuidToAlias</b> function is available on Windows Vista
  
   and later.

The <b>ConvertInterfaceLuidToAlias</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol.

The maximum length of the alias name for a network interface, <b>NDIS_IF_MAX_STRING_SIZE</b>, without the terminating <b>NULL</b> is declared in the <i>Ntddndis.h</i> header file. The <b>NDIS_IF_MAX_STRING_SIZE</b> is defined to be the <b>IF_MAX_STRING_SIZE</b> constant defined in the <i>Ifdef.h</i> header file. The <i>Ntddndis.h</i> and <i>Ifdef.h</i> header files are automatically included in the <i>Netioapi.h</i> header file which is automatically included by the <i>Iphlpapi.h</i> header file. The <i>Ntddndis.h</i>, <i>Ifdef.h</i>, and <i> Netioapi.h</i> header files should never be used directly. 





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546130">ConvertInterfaceAliasToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546137">ConvertInterfaceGuidToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546141">ConvertInterfaceIndexToLuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546156">ConvertInterfaceLuidToGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546167">ConvertInterfaceLuidToIndex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546171">ConvertInterfaceLuidToNameA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546175">ConvertInterfaceLuidToNameW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546185">ConvertInterfaceNameToLuidA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546192">ConvertInterfaceNameToLuidW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553785">if_indextoname</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553788">if_nametoindex</a>
 

 

