---
UID: NF:netioapi.if_indextoname
title: if_indextoname function (netioapi.h)
description: Converts the local index for a network interface to the ANSI interface name.
helpviewer_keywords: ["if_indextoname","if_indextoname function [IP Helper]","iphlp.if_indextoname","netioapi/if_indextoname"]
old-location: iphlp\if_indextoname.htm
tech.root: IpHlp
ms.assetid: 0da31819-3ee7-4474-9e68-f5a18d4a135a
ms.date: 12/05/2018
ms.keywords: if_indextoname, if_indextoname function [IP Helper], iphlp.if_indextoname, netioapi/if_indextoname
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - if_indextoname
 - netioapi/if_indextoname
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - if_indextoname
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

The <b>if_indextoname</b> function is available on Windows Vista and later.

The <b>if_indextoname</b> function maps an interface index into its corresponding
   name. This function is designed as part of basic socket extensions for IPv6 as described by the IETF in RFC 2553. For more information, see <a href="http://tools.ietf.org/html/rfc2553">http://www.ietf.org/rfc/rfc2553.txt</a>. 

The <b>if_indextoname</b> function is implemented for portability of applications with Unix environments, but the ConvertInterface functions are preferred. The <b>if_indextoname</b> function can be replaced by a call to the <a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceindextoluid">ConvertInterfaceIndexToLuid</a> function to convert an interface index to a  <a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a> followed by a call to the <a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a> to convert the NET_LUID to the ANSI interface name.

If the <b>if_indextoname</b> fails and returns a <b>NULL</b> pointer, it is not possible to determine an error code. 

The length, in bytes, of the buffer pointed to by the <i>InterfaceName</i> parameter must be equal or greater than <b>IF_NAMESIZE</b>, a value declared in the <i>Netioapi.h</i> header file equal to <b>NDIS_IF_MAX_STRING_SIZE</b>. The maximum length of an interface name, <b>NDIS_IF_MAX_STRING_SIZE</b>, without the terminating <b>NULL</b> is declared in the <i>Ntddndis.h</i> header file. The <b>NDIS_IF_MAX_STRING_SIZE</b> is defined to be the <b>IF_MAX_STRING_SIZE</b> constant defined in the <i>Ifdef.h</i> header file. The <i>Ntddndis.h</i> and <i>Ifdef.h</i> header files are automatically included in the <i>Netioapi.h</i> header file which is automatically included by the <i>Iphlpapi.h</i> header file. The <i>Ntddndis.h</i>, <i>Ifdef.h</i>, and <i> Netioapi.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacealiastoluid">ConvertInterfaceAliasToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceguidtoluid">ConvertInterfaceGuidToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceindextoluid">ConvertInterfaceIndexToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoalias">ConvertInterfaceLuidToAlias</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoguid">ConvertInterfaceLuidToGuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoindex">ConvertInterfaceLuidToIndex</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamew">ConvertInterfaceLuidToNameW</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluida">ConvertInterfaceNameToLuidA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluidw">ConvertInterfaceNameToLuidW</a>



<a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_nametoindex">if_nametoindex</a>