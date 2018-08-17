---
UID: NF:netioapi.ConvertInterfaceLuidToGuid
title: ConvertInterfaceLuidToGuid function
author: windows-sdk-content
description: Converts a locally unique identifier (LUID) for a network interface to a globally unique identifier (GUID) for the interface.
old-location: iphlp\convertinterfaceluidtoguid.htm
old-project: iphlp
ms.assetid: 9d5bd1e9-0bf1-405a-8726-8e2c9ba4e022
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: ConvertInterfaceLuidToGuid, ConvertInterfaceLuidToGuid function [IP Helper], iphlp.convertinterfaceluidtoguid, netioapi/ConvertInterfaceLuidToGuid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.redist: 
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
 - ConvertInterfaceLuidToGuid
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ConvertInterfaceLuidToGuid function


## -description


The 
<b>ConvertInterfaceLuidToGuid</b> function converts a locally unique identifier (LUID) for a network interface to a globally unique identifier (GUID) for the interface.


## -parameters




### -param InterfaceLuid [in]

A pointer to a <a href="https://msdn.microsoft.com/c4956c5a-3c6c-4f1c-b9d7-2e377b66f197">NET_LUID</a> for a network interface.


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



The <b>ConvertInterfaceLuidToGuid</b> function is available on Windows Vistaand later.

The <b>ConvertInterfaceLuidToGuid</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol.




## -see-also




<a href="https://msdn.microsoft.com/7fa80938-d475-4ace-b463-a53aac26e88b">ConvertInterfaceAliasToLuid</a>



<a href="https://msdn.microsoft.com/cae669dc-899b-4485-b70a-5f58207a07df">ConvertInterfaceGuidToLuid</a>



<a href="https://msdn.microsoft.com/c757228c-93f1-4545-8921-9d048bca580c">ConvertInterfaceIndexToLuid</a>



<a href="https://msdn.microsoft.com/86a821c1-e04b-4bc3-846d-767c55008aed">ConvertInterfaceLuidToAlias</a>



<a href="https://msdn.microsoft.com/904cd94c-dd46-42ac-aef2-ffed4b3e5899">ConvertInterfaceLuidToIndex</a>



<a href="https://msdn.microsoft.com/c65f7b3c-55f4-40f8-9a7a-19d1066deca4">ConvertInterfaceLuidToNameA</a>



<a href="https://msdn.microsoft.com/e4269a6a-1237-4503-b7d7-756388458750">ConvertInterfaceLuidToNameW</a>



<a href="https://msdn.microsoft.com/daceabf9-ff43-4206-9f8f-f3924de9c5a5">ConvertInterfaceNameToLuidA</a>



<a href="https://msdn.microsoft.com/473be9f0-7fac-46f0-b33c-839906411fdc">ConvertInterfaceNameToLuidW</a>



<a href="https://msdn.microsoft.com/c4956c5a-3c6c-4f1c-b9d7-2e377b66f197">NET_LUID</a>



<a href="https://msdn.microsoft.com/0da31819-3ee7-4474-9e68-f5a18d4a135a">if_indextoname</a>



<a href="https://msdn.microsoft.com/599e5a34-1e17-4c5f-b58e-727871e409be">if_nametoindex</a>
 

 

