---
UID: NF:netioapi.if_indextoname
title: if_indextoname function
author: windows-sdk-content
description: Converts the local index for a network interface to the ANSI interface name.
old-location: iphlp\if_indextoname.htm
tech.root: IpHlp
ms.assetid: 0da31819-3ee7-4474-9e68-f5a18d4a135a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: if_indextoname, if_indextoname function [IP Helper], iphlp.if_indextoname, netioapi/if_indextoname
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
 - if_indextoname
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# if_indextoname function


## -description


The 
<b>if_indextoname</b> function converts the local index for a network interface to the ANSI interface name.


## -parameters




### -param InterfaceIndex [in]

The local index for a network interface.


### -param InterfaceName [out]

A pointer to a buffer to hold the <b>NULL</b>-terminated ANSI string containing the interface name when the function returns successfully. The length, in bytes, of the buffer pointed to by this parameter must be equal to or greater than 
        <b>IF_NAMESIZE</b>.


## -returns



On success, 
<b>if_indextoname</b> returns a pointer to <b>NULL</b>-terminated ANSI string containing the interface name. On failure, a <b>NULL</b> pointer is returned.  




## -remarks



The <b>if_indextoname</b> function is available on Windows Vistaand later.

The <b>if_indextoname</b> function maps an interface index into its corresponding
   name. This function is designed as part of basic socket extensions for IPv6 as described by the IETF in RFC 2553. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=86448">http://www.ietf.org/rfc/rfc2553.txt</a>. 

The <b>if_indextoname</b> function is implemented for portability of applications with Unix environments, but the ConvertInterface functions are preferred. The <b>if_indextoname</b> function can be replaced by a call to the <a href="https://msdn.microsoft.com/c757228c-93f1-4545-8921-9d048bca580c">ConvertInterfaceIndexToLuid</a> function to convert an interface index to a  <a href="https://msdn.microsoft.com/c4956c5a-3c6c-4f1c-b9d7-2e377b66f197">NET_LUID</a> followed by a call to the <a href="https://msdn.microsoft.com/c65f7b3c-55f4-40f8-9a7a-19d1066deca4">ConvertInterfaceLuidToNameA</a> to convert the NET_LUID to the ANSI interface name.

If the <b>if_indextoname</b> fails and returns a <b>NULL</b> pointer, it is not possible to determine an error code. 

The length, in bytes, of the buffer pointed to by the <i>InterfaceName</i> parameter must be equal or greater than <b>IF_NAMESIZE</b>, a value declared in the <i>Netioapi.h</i> header file equal to <b>NDIS_IF_MAX_STRING_SIZE</b>. The maximum length of an interface name, <b>NDIS_IF_MAX_STRING_SIZE</b>, without the terminating <b>NULL</b> is declared in the <i>Ntddndis.h</i> header file. The <b>NDIS_IF_MAX_STRING_SIZE</b> is defined to be the <b>IF_MAX_STRING_SIZE</b> constant defined in the <i>Ifdef.h</i> header file. The <i>Ntddndis.h</i> and <i>Ifdef.h</i> header files are automatically included in the <i>Netioapi.h</i> header file which is automatically included by the <i>Iphlpapi.h</i> header file. The <i>Ntddndis.h</i>, <i>Ifdef.h</i>, and <i> Netioapi.h</i> header files should never be used directly. 





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



<a href="https://msdn.microsoft.com/599e5a34-1e17-4c5f-b58e-727871e409be">if_nametoindex</a>
 

 

