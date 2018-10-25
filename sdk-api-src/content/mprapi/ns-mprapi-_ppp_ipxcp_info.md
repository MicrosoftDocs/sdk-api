---
UID: NS:mprapi._PPP_IPXCP_INFO
title: "_PPP_IPXCP_INFO"
author: windows-sdk-content
description: The PPP_IPXCP_INFO structure contains the result of a PPP Internetwork Packet Exchange (IPX) projection operation.
old-location: rras\ppp_ipxcp_info.htm
tech.root: rras
ms.assetid: 6e269c4e-8014-4d59-a7dc-3314a67a4d12
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: PPP_IPXCP_INFO, PPP_IPXCP_INFO structure [RAS], _PPP_IPXCP_INFO, _mpr_ppp_ipxcp_info, mprapi/PPP_IPXCP_INFO, rras.ppp_ipxcp_info
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPP_IPXCP_INFO
product: Windows
targetos: Windows
req.typenames: PPP_IPXCP_INFO
req.redist: 
---

# _PPP_IPXCP_INFO structure


## -description


The 
<b>PPP_IPXCP_INFO</b> structure contains the result of a PPP Internetwork Packet Exchange (IPX) projection operation.


## -struct-fields




### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.


### -field wszAddress

Specifies a Unicode string that holds the client's IPX address on the RAS connection. This address string has the form <i>net</i><b>.</b><i>node</i>, for example, "1234ABCD.12AB34CD56EF".


## -remarks



The 
<b>PPP_IPXCP_INFO</b> structure can be used only when administrating computers that are running 32-bit Windows Server 2003 or an earlier operating system. Windows 2000 64-bit Edition does not support the IPX protocol.




## -see-also




<a href="https://msdn.microsoft.com/39692a38-ab40-43da-a704-8c206be72ceb">PPP_INFO</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

