---
UID: NE:tcpmib.TCP_CONNECTION_OFFLOAD_STATE
title: TCP_CONNECTION_OFFLOAD_STATE
author: windows-driver-content
description: Defines the possible TCP offload states for a TCP connection.
old-location: mib\tcp_connection_offload_state.htm
old-project: MIB
ms.assetid: cef633e7-1577-4f10-bd14-8d8e85aa78e6
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "*PTCP_CONNECTION_OFFLOAD_STATE, TCP_CONNECTION_OFFLOAD_STATE, TCP_CONNECTION_OFFLOAD_STATE enumeration [MIB], TcpConnectionOffloadStateInHost, TcpConnectionOffloadStateMax, TcpConnectionOffloadStateOffloaded, TcpConnectionOffloadStateOffloading, TcpConnectionOffloadStateUploading, iprtrmib/TCP_CONNECTION_OFFLOAD_STATE, iprtrmib/TcpConnectionOffloadStateInHost, iprtrmib/TcpConnectionOffloadStateMax, iprtrmib/TcpConnectionOffloadStateOffloaded, iprtrmib/TcpConnectionOffloadStateOffloading, iprtrmib/TcpConnectionOffloadStateUploading, mib.tcp_connection_offload_state, tcpmib/TCP_CONNECTION_OFFLOAD_STATE, tcpmib/TcpConnectionOffloadStateInHost, tcpmib/TcpConnectionOffloadStateMax, tcpmib/TcpConnectionOffloadStateOffloaded, tcpmib/TcpConnectionOffloadStateOffloading, tcpmib/TcpConnectionOffloadStateUploading"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tcpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TCP_CONNECTION_OFFLOAD_STATE, *PTCP_CONNECTION_OFFLOAD_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tcpmib.h
-	Iprtrmib.h
api_name:
-	TCP_CONNECTION_OFFLOAD_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TCP_CONNECTION_OFFLOAD_STATE enumeration


## -description


The <b>TCP_CONNECTION_OFFLOAD_STATE</b> enumeration defines the possible TCP offload states for a TCP connection. 


## -enum-fields




### -field TcpConnectionOffloadStateInHost

The TCP connection is currently owned by the network stack on the local computer, and is not offloaded



### -field TcpConnectionOffloadStateOffloading

The TCP connection is in the process of being offloaded, but the offload has not been completed.


### -field TcpConnectionOffloadStateOffloaded

The TCP connection is offloaded to the network interface controller.


### -field TcpConnectionOffloadStateUploading

The TCP connection is in the process of being uploaded back to the network stack on the local computer, but the reinstate-to-host process has not completed. 



### -field TcpConnectionOffloadStateMax

The maximum possible value for the <a href="https://msdn.microsoft.com/cef633e7-1577-4f10-bd14-8d8e85aa78e6">TCP_CONNECTION_OFFLOAD_STATE</a> enumeration type. This is not a legal value for the possible TCP connection offload state.


## -remarks



The <b>TCP_CONNECTION_OFFLOAD_STATE</b> enumeration is defined on Windows Server 2003 and later. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>TCP_CONNECTION_OFFLOAD_STATE</b> enumeration  is defined in the <i>Tcpmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/77150609-d06d-4492-bbd7-21eecd825bde">GetTcp6Table</a>



<a href="https://msdn.microsoft.com/435b9198-b921-407c-9441-31cfe77c03f1">GetTcp6Table2</a>



<a href="https://msdn.microsoft.com/bbec3397-0317-40f7-926f-2ec48cf5386d">MIB_TCP6ROW2</a>



<a href="https://msdn.microsoft.com/3cb8568e-ce31-4ed1-aa9e-abcb826c0cea">MIB_TCP6TABLE2</a>



<a href="https://msdn.microsoft.com/cff343cd-fe85-4e60-87bd-c1e9833cea38">MIB_TCPROW2</a>



<a href="https://msdn.microsoft.com/e07de994-0bd5-4d18-9012-8ff191dd6939">MIB_TCPTABLE2</a>
 

 

