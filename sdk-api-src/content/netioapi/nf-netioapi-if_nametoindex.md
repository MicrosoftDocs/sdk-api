---
UID: NF:netioapi.if_nametoindex
title: if_nametoindex function
author: windows-sdk-content
description: Converts the ANSI interface name for a network interface to the local index for the interface.
old-location: iphlp\if_nametoindex.htm
old-project: IpHlp
ms.assetid: 599e5a34-1e17-4c5f-b58e-727871e409be
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: if_nametoindex, if_nametoindex function [IP Helper], iphlp.if_nametoindex, netioapi/if_nametoindex
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
 - if_nametoindex
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



The <b>if_nametoindex</b> function is available on Windows Vista
  
   and later.

The <b>if_nametoindex</b> function maps an interface name into its corresponding
   index. This function is designed as part of basic socket extensions for IPv6 as described by the IETF in RFC 2553. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=86448">http://www.ietf.org/rfc/rfc2553.txt</a>. 

The <b>if_nametoindex</b> function is implemented for portability of applications with Unix environments, but the ConvertInterface functions are preferred. The <b>if_nametoindex</b> function can be replaced by a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546185">ConvertInterfaceNameToLuidA</a> function to convert the ANSI interface name to a  <a href="https://msdn.microsoft.com/library/windows/hardware/ff568747">NET_LUID</a> followed by a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546167">ConvertInterfaceLuidToIndex</a> to convert the NET_LUID to the local interface index.

If the <b>if_nametoindex</b> function fails and returns zero, it is not possible to determine an error code. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546130">ConvertInterfaceAliasToLuid</a>



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
 

 

