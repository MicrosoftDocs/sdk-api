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

The <b>if_nametoindex</b> function is implemented for portability of applications with Unix environments, but the ConvertInterface functions are preferred. The <b>if_nametoindex</b> function can be replaced by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluida">ConvertInterfaceNameToLuidA</a> function to convert the ANSI interface name to a  <a href="https://docs.microsoft.com/windows/desktop/api/ifdef/ns-ifdef-_net_luid_lh">NET_LUID</a> followed by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoindex">ConvertInterfaceLuidToIndex</a> to convert the NET_LUID to the local interface index.

If the <b>if_nametoindex</b> function fails and returns zero, it is not possible to determine an error code. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfacealiastoluid">ConvertInterfaceAliasToLuid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceguidtoluid">ConvertInterfaceGuidToLuid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceindextoluid">ConvertInterfaceIndexToLuid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoalias">ConvertInterfaceLuidToAlias</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoguid">ConvertInterfaceLuidToGuid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoindex">ConvertInterfaceLuidToIndex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamew">ConvertInterfaceLuidToNameW</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluida">ConvertInterfaceNameToLuidA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluidw">ConvertInterfaceNameToLuidW</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ifdef/ns-ifdef-_net_luid_lh">NET_LUID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-if_indextoname">if_indextoname</a>
 

 

