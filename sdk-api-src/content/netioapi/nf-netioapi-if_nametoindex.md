---
UID: NF:netioapi.if_nametoindex
title: if_nametoindex function (netioapi.h)
author: windows-sdk-content
description: Converts the ANSI interface name for a network interface to the local index for the interface.
old-location: iphlp\if_nametoindex.htm
tech.root: IpHlp
ms.assetid: 599e5a34-1e17-4c5f-b58e-727871e409be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: if_nametoindex, if_nametoindex function [IP Helper], iphlp.if_nametoindex, netioapi/if_nametoindex
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
 - if_nametoindex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# if_nametoindex function


## -description


The 
<b>if_nametoindex</b> function converts the ANSI interface name for a network interface to the local index for the interface.


## -parameters




### -param InterfaceName [in]

A pointer to a <b>NULL</b>-terminated ANSI string containing the interface name.


## -returns



On success, 
<b>if_nametoindex</b> returns the local interface index. On failure, zero is returned.  




## -remarks



The <b>if_nametoindex</b> function is available on Windows Vistaand later.

The <b>if_nametoindex</b> function maps an interface name into its corresponding
   index. This function is designed as part of basic socket extensions for IPv6 as described by the IETF in RFC 2553. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=86448">http://www.ietf.org/rfc/rfc2553.txt</a>. 

The <b>if_nametoindex</b> function is implemented for portability of applications with Unix environments, but the ConvertInterface functions are preferred. The <b>if_nametoindex</b> function can be replaced by a call to the <a href="https://msdn.microsoft.com/daceabf9-ff43-4206-9f8f-f3924de9c5a5">ConvertInterfaceNameToLuidA</a> function to convert the ANSI interface name to a  <a href="https://msdn.microsoft.com/c4956c5a-3c6c-4f1c-b9d7-2e377b66f197">NET_LUID</a> followed by a call to the <a href="https://msdn.microsoft.com/904cd94c-dd46-42ac-aef2-ffed4b3e5899">ConvertInterfaceLuidToIndex</a> to convert the NET_LUID to the local interface index.

If the <b>if_nametoindex</b> function fails and returns zero, it is not possible to determine an error code. 




## -see-also




<a href="https://msdn.microsoft.com/7fa80938-d475-4ace-b463-a53aac26e88b">ConvertInterfaceAliasToLuid</a>



<a href="https://msdn.microsoft.com/cae669dc-899b-4485-b70a-5f58207a07df">ConvertInterfaceGuidToLuid</a>



<a href="https://msdn.microsoft.com/c757228c-93f1-4545-8921-9d048bca580c">ConvertInterfaceIndexToLuid</a>



<a href="https://msdn.microsoft.com/86a821c1-e04b-4bc3-846d-767c55008aed">ConvertInterfaceLuidToAlias</a>



<a href="https://msdn.microsoft.com/9d5bd1e9-0bf1-405a-8726-8e2c9ba4e022">ConvertInterfaceLuidToGuid</a>



<a href="https://msdn.microsoft.com/904cd94c-dd46-42ac-aef2-ffed4b3e5899">ConvertInterfaceLuidToIndex</a>



<a href="https://msdn.microsoft.com/c65f7b3c-55f4-40f8-9a7a-19d1066deca4">ConvertInterfaceLuidToNameA</a>



<a href="https://msdn.microsoft.com/e4269a6a-1237-4503-b7d7-756388458750">ConvertInterfaceLuidToNameW</a>



<a href="https://msdn.microsoft.com/daceabf9-ff43-4206-9f8f-f3924de9c5a5">ConvertInterfaceNameToLuidA</a>



<a href="https://msdn.microsoft.com/473be9f0-7fac-46f0-b33c-839906411fdc">ConvertInterfaceNameToLuidW</a>



<a href="https://msdn.microsoft.com/c4956c5a-3c6c-4f1c-b9d7-2e377b66f197">NET_LUID</a>



<a href="https://msdn.microsoft.com/0da31819-3ee7-4474-9e68-f5a18d4a135a">if_indextoname</a>
 

 

