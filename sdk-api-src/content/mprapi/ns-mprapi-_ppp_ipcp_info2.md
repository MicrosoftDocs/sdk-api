---
UID: NS:mprapi._PPP_IPCP_INFO2
title: "_PPP_IPCP_INFO2"
author: windows-driver-content
description: The PPP_IPCP_INFO2 structure contains the result of a PPP Internet Protocol (IP) negotiation.
old-location: rras\ppp_ipcp_info2.htm
old-project: RRAS
ms.assetid: e12cde70-51af-484b-a700-f3976a3abc4a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PPP_IPCP_INFO2, PPP_IPCP_INFO2 structure [RAS], _PPP_IPCP_INFO2, _mpr_ppp_ipcp_info2, mprapi/PPP_IPCP_INFO2, rras.ppp_ipcp_info2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PPP_IPCP_INFO2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mprapi.h
api_name:
-	PPP_IPCP_INFO2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _PPP_IPCP_INFO2 structure


## -description


The 
<b>PPP_IPCP_INFO2</b> structure contains the result of a PPP Internet Protocol (IP) negotiation.


## -struct-fields




### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.


### -field wszAddress

Specifies a Unicode string that holds the local computer's IP address for the connection. This string has the form <i>a</i><b>.</b><i>b</i><b>.</b><i>c</i><b>.</b><i>d</i>; for example, "10.102.235.84". 




The 
<b>PPP_IPCP_INFO2</b> structures provides address information from the perspective of the server. For example, if a remote access client is connecting to a RAS server, this member holds the IP address of the server.


### -field wszRemoteAddress

Specifies a Unicode string that holds the IP address of the remote computer. This string has the form <i>a</i><b>.</b><i>b</i><b>.</b><i>c</i><b>.</b><i>d</i>. If the address is not available, this member specifies an empty string. 




The 
<b>PPP_IPCP_INFO2</b> structures provides address information from the perspective of the server. For example, if a remote access client is connecting to a RAS server, this member holds the IP address of the client.


### -field dwOptions

Specifies IPCP options for the local computer. Currently, the only option is PPP_IPCP_VJ. This option indicates that IP datagrams sent by the local computer are compressed using Van Jacobson compression.


### -field dwRemoteOptions

Specifies IPCP options for the remote peer. Currently, the only option is PPP_IPCP_VJ. This option indicates that IP datagrams sent by the remote peer (that is, received by the local computer) are compressed using Van Jacobson compression.


## -see-also




<a href="https://msdn.microsoft.com/39692a38-ab40-43da-a704-8c206be72ceb">PPP_INFO</a>



<a href="https://msdn.microsoft.com/c77f54d2-eac4-4e0a-92c5-c46d521a272d">PPP_IPCP_INFO</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

