---
UID: NS:iptypes._IP_ADAPTER_WINS_SERVER_ADDRESS_LH
title: "_IP_ADAPTER_WINS_SERVER_ADDRESS_LH"
author: windows-sdk-content
description: Stores a single Windows Internet Name Service (WINS) server address in a linked list of WINS server addresses for a particular adapter.
old-location: iphlp\ip_adapter_wins_server_address.htm
tech.root: iphlp
ms.assetid: AF9A40C4-63DB-4830-A689-1DFE4DC2CAB7
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: "*PIP_ADAPTER_WINS_SERVER_ADDRESS, *PIP_ADAPTER_WINS_SERVER_ADDRESS_LH, IP_ADAPTER_WINS_SERVER_ADDRESS, IP_ADAPTER_WINS_SERVER_ADDRESS structure [IP Helper], IP_ADAPTER_WINS_SERVER_ADDRESS_LH, PIP_ADAPTER_WINS_SERVER_ADDRESS, PIP_ADAPTER_WINS_SERVER_ADDRESS structure pointer [IP Helper], _IP_ADAPTER_WINS_SERVER_ADDRESS_LH, iphlp.ip_adapter_wins_server_address, iptypes/IP_ADAPTER_WINS_SERVER_ADDRESS, iptypes/PIP_ADAPTER_WINS_SERVER_ADDRESS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iptypes.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iptypes.h
api_name:
 - IP_ADAPTER_WINS_SERVER_ADDRESS
product: Windows
targetos: Windows
req.typenames: IP_ADAPTER_WINS_SERVER_ADDRESS_LH, *PIP_ADAPTER_WINS_SERVER_ADDRESS_LH
req.redist: 
---

# _IP_ADAPTER_WINS_SERVER_ADDRESS_LH structure


## -description


The 
<b>IP_ADAPTER_WINS_SERVER_ADDRESS</b> structure stores a single Windows Internet Name Service (WINS) server address in a linked list of WINS server addresses for a particular adapter.


## -struct-fields




### -field Alignment

Reserved. Used by the compiler to align the structure.


### -field Length

The length, in bytes, of this structure.


### -field Reserved

Reserved. 
							


### -field Next

A pointer to the next WINS server address structure in the list.


### -field Address

The IP address for this WINS server entry. This member can be an IPv6 address or an IPv4 address. 


## -remarks



The <a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a> structure is retrieved by the <a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a> function. The <b>FirstWinsServerAddress</b> member of the <b>IP_ADAPTER_ADDRESSES</b>structure is a pointer to a linked list of <b>IP_ADAPTER_WINS_SERVER_ADDRESS</b> structures. 

The <a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a> structure is used in the <a href="https://msdn.microsoft.com/CA38504A-1CC9-4ABA-BD4E-1B2EAD6F588B">IP_ADAPTER_GATEWAY_ADDRESS</a> structure. On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>SOCKET_ADDRESS</b> structure is defined in the <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. On the Platform Software Development Kit (SDK) released for Windows Server 2003 and Windows XP, the <b>SOCKET_ADDRESS</b> structure is declared in the <i>Winsock2.h</i> header file. In order to use the <b>IP_ADAPTER_GATEWAY_ADDRESS</b> structure, the <i>Winsock2.h</i> header file must be included before the <i>Iphlpapi.h</i> header file.  




## -see-also




<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>



<a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a>
 

 

