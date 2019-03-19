---
UID: NE:tcpestats._TCP_BOOLEAN_OPTIONAL
title: TCP_BOOLEAN_OPTIONAL (tcpestats.h)
author: windows-sdk-content
description: Defines the states that a caller can specify when updating a member in the read/write information for a TCP connection.
old-location: iphlp\tcp_boolean_optional.htm
tech.root: IpHlp
ms.assetid: 68f8f797-06fb-4286-88bc-220c54977575
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTCP_BOOLEAN_OPTIONAL, TCP_BOOLEAN_OPTIONAL, TCP_BOOLEAN_OPTIONAL enumeration [IP Helper], TcpBoolOptDisabled, TcpBoolOptEnabled, TcpBoolOptUnchanged, iphlp.tcp_boolean_optional, tcpestats/TCP_BOOLEAN_OPTIONAL, tcpestats/TcpBoolOptDisabled, tcpestats/TcpBoolOptEnabled, tcpestats/TcpBoolOptUnchanged"
ms.topic: enum
req.header: tcpestats.h
req.include-header: 
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
 - Tcpestats.h
api_name:
 - TCP_BOOLEAN_OPTIONAL
product: Windows
targetos: Windows
req.typenames: TCP_BOOLEAN_OPTIONAL, *PTCP_BOOLEAN_OPTIONAL
req.redist: 
---

# TCP_BOOLEAN_OPTIONAL enumeration


## -description


The <b>TCP_BOOLEAN_OPTIONAL</b> enumeration defines the states that a caller can specify when updating a member in the read/write information for a TCP connection.


## -enum-fields




### -field TcpBoolOptDisabled

The option should be disabled. 


### -field TcpBoolOptEnabled

The option should be enabled. 


### -field TcpBoolOptUnchanged

The option should be unchanged. 


## -remarks



The <b>TCP_BOOLEAN_OPTIONAL</b> enumeration is defined on Windows Vista and later. 

The collection of extended statistics on a TCP connection are enabled and disabled using calls to the <a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a> and <a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a> functions where the type of extended statistics specified is one of values from the <a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a> enumeration type. A value from the <b>TCP_BOOLEAN_OPTIONAL</b> enumeration is used to specify how a member in the <a href="https://msdn.microsoft.com/a9bf5ad3-a8db-4194-8e47-5a7409391f4c">TCP_ESTATS_BANDWIDTH_RW_v0</a> structure should be updated to enable or disable extended statistics on a TCP connection for bandwidth estimation. 




## -see-also




<a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/a9bf5ad3-a8db-4194-8e47-5a7409391f4c">TCP_ESTATS_BANDWIDTH_RW_v0</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

