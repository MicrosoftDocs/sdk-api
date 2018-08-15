---
UID: NE:iphlpapi.NET_ADDRESS_FORMAT_
title: NET_ADDRESS_FORMAT_
author: windows-sdk-content
description: The NET_ADDRESS_FORMAT enumeration specifies the format of a network address returned by the ParseNetworkString function.
old-location: iphlp\net_address_format.htm
old-project: iphlp
ms.assetid: a99df758-d46e-452d-acf8-d2cb5a6fa22e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NET_ADDRESS_DNS_NAME, NET_ADDRESS_FORMAT, NET_ADDRESS_FORMAT enumeration [IP Helper], NET_ADDRESS_FORMAT_, NET_ADDRESS_FORMAT_UNSPECIFIED, NET_ADDRESS_IPV4, NET_ADDRESS_IPV6, iphlp.net_address_format, iphlpapi/NET_ADDRESS_DNS_NAME, iphlpapi/NET_ADDRESS_FORMAT, iphlpapi/NET_ADDRESS_FORMAT_UNSPECIFIED, iphlpapi/NET_ADDRESS_IPV4, iphlpapi/NET_ADDRESS_IPV6
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iphlpapi.h
req.include-header: 
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iphlpapi.h
api_name:
 - NET_ADDRESS_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# NET_ADDRESS_FORMAT_ enumeration


## -description


The <b>NET_ADDRESS_FORMAT</b> enumeration specifies the format of a network address returned by the <a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a> function.


## -enum-fields




### -field NET_ADDRESS_FORMAT_UNSPECIFIED

The format of the network address is unspecified.


### -field NET_ADDRESS_DNS_NAME

The format of the network address is a DNS name.


### -field NET_ADDRESS_IPV4

The format of the network address is a string in Internet standard dotted-decimal notation for IPv4.



### -field NET_ADDRESS_IPV6

The format of the network address is a string in Internet standard hexadecimal encoding for IPv6.



## -remarks



The <b>NET_ADDRESS_FORMAT</b> enumeration is defined on Windows Vista and later. 

The <b>NET_ADDRESS_FORMAT</b> enumeration is used in the <a href="https://msdn.microsoft.com/1a59cc13-a3fc-4489-aafd-444a96d9a339">NET_ADDRESS_INFO</a> structure returned by the <a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/1a59cc13-a3fc-4489-aafd-444a96d9a339">NET_ADDRESS_INFO</a>



<a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a>
 

 

