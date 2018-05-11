---
UID: NS:tcpestats._TCP_ESTATS_PATH_RW_v0
title: "_TCP_ESTATS_PATH_RW_v0"
author: windows-driver-content
description: Contains read/write configuration information for extended TCP statistics on path measurement for a TCP connection.
old-location: iphlp\tcp_estats_path_rw_v0.htm
old-project: IpHlp
ms.assetid: 460ad710-06aa-490a-9bac-5a8c731687e9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PTCP_ESTATS_PATH_RW_v0, PTCP_ESTATS_PATH_RW_v0, PTCP_ESTATS_PATH_RW_v0 structure pointer [IP Helper], TCP_ESTATS_PATH_RW_v0, TCP_ESTATS_PATH_RW_v0 structure [IP Helper], _TCP_ESTATS_PATH_RW_v0, iphlp.tcp_estats_path_rw_v0, tcpestats/PTCP_ESTATS_PATH_RW_v0, tcpestats/TCP_ESTATS_PATH_RW_v0"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: TCP_ESTATS_PATH_RW_v0, *PTCP_ESTATS_PATH_RW_v0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tcpestats.h
api_name:
-	TCP_ESTATS_PATH_RW_v0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _TCP_ESTATS_PATH_RW_v0 structure


## -description


The <b>TCP_ESTATS_PATH_RW_v0</b> structure contains read/write configuration information for extended TCP statistics on path measurement for a TCP connection.


## -struct-fields




### -field EnableCollection

A value that indicates if extended statistics on a TCP connection should be collected for path measurement information. 

If this member is set to <b>TRUE</b>, extended statistics on the TCP connection are enabled. If this member is set to <b>FALSE</b>, extended statistics on the TCP connection are disabled. 

The default state for this member when not set is disabled.


## -remarks



The <b>TCP_ESTATS_PATH_RW_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_PATH_RW_v0</b> is defined as version 0 of the structure for  read/write configuration information on extended path measurement for a TCP connection.  This information is used to infer segment reordering on the path from the local sender to the remote receiver. 

Extended TCP statistics on extended path measurement information for a TCP connection are enabled and disabled using this structure and the <a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a> and <a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsPath</b> is passed in the <i>EstatsType</i> parameter.

The <b>TCP_ESTATS_PATH_RW_v0</b> structure is retrieved by calls to  the <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> or <a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsPath</b> is passed in the <i>EstatsType</i> parameter. 




## -see-also




<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

