---
UID: NS:netioapi._IP_ADDRESS_PREFIX
title: "_IP_ADDRESS_PREFIX"
author: windows-sdk-content
description: Stores an IP address prefix.
old-location: iphlp\ip_address_prefix.htm
tech.root: iphlp
ms.assetid: 3a6598d8-77e4-46f7-9397-124157508207
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: "*PIP_ADDRESS_PREFIX, IP_ADDRESS_PREFIX, IP_ADDRESS_PREFIX structure [IP Helper], PIP_ADDRESS_PREFIX, PIP_ADDRESS_PREFIX structure pointer [IP Helper], _IP_ADDRESS_PREFIX, iphlp.ip_address_prefix, netioapi/IP_ADDRESS_PREFIX, netioapi/PIP_ADDRESS_PREFIX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - IP_ADDRESS_PREFIX
product: Windows
targetos: Windows
req.typenames: IP_ADDRESS_PREFIX, *PIP_ADDRESS_PREFIX
req.redist: 
---

# _IP_ADDRESS_PREFIX structure


## -description


The <b>IP_ADDRESS_PREFIX</b> structure  stores an IP address prefix.


## -struct-fields




### -field Prefix

The prefix or network part of IP the address represented as an IP address.

The <a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a> union is defined in the <i>Ws2ipdef.h</i> header. 


### -field PrefixLength

The length, in bits, of the prefix or network part of the IP address. For a unicast IPv4 address, any value greater than 32 is an illegal value. For a unicast IPv6 address, any value greater than 128 is an illegal value. 
A value of 255 is commonly used to represent an illegal value. 


## -remarks



The <b>IP_ADDRESS_PREFIX</b> structure is defined on Windows Vista and later. 

The <b>IP_ADDRESS_PREFIX</b> structure is the data type of the <b>DestinationPrefix</b> member in the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure.  A number of functions use the <b>MIB_IPFORWARD_ROW2</b> structure including <a href="https://msdn.microsoft.com/d2d065d3-daad-4167-8b87-4229199ee76a">CreateIpForwardEntry2</a>, <a href="https://msdn.microsoft.com/68d5a5a5-21cf-4337-8a35-7f847f5e2138">DeleteIpForwardEntry2</a>, <a href="https://msdn.microsoft.com/7bc16824-c98f-4cd5-a589-e198b48b637c">GetBestRoute2</a>, <a href="https://msdn.microsoft.com/53d5009a-d205-40ce-88e5-fe37e72b5a50">GetIpForwardEntry2</a>, <a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a>, <a href="https://msdn.microsoft.com/1968c4e5-4b28-4387-a918-3326bc80bb3e">InitializeIpForwardEntry</a>, <a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a>, and <a href="https://msdn.microsoft.com/e11aab0b-6d6c-4e90-a60a-f7d68c09751b">SetIpForwardEntry2</a>.




## -see-also




<a href="https://msdn.microsoft.com/d2d065d3-daad-4167-8b87-4229199ee76a">CreateIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/68d5a5a5-21cf-4337-8a35-7f847f5e2138">DeleteIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/7bc16824-c98f-4cd5-a589-e198b48b637c">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/53d5009a-d205-40ce-88e5-fe37e72b5a50">GetIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/1968c4e5-4b28-4387-a918-3326bc80bb3e">InitializeIpForwardEntry</a>



<a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a>



<a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a>



<a href="https://msdn.microsoft.com/e11aab0b-6d6c-4e90-a60a-f7d68c09751b">SetIpForwardEntry2</a>
 

 

