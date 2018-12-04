---
UID: NS:mprapi._PPP_INFO
title: "_PPP_INFO"
author: windows-sdk-content
description: The PPP_INFO structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.
old-location: rras\ppp_info.htm
tech.root: rras
ms.assetid: 39692a38-ab40-43da-a704-8c206be72ceb
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: PPP_INFO, PPP_INFO structure [RAS], _PPP_INFO, _mpr_ppp_info, mprapi/PPP_INFO, rras.ppp_info
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
 - PPP_INFO
product: Windows
targetos: Windows
req.typenames: PPP_INFO
req.redist: 
---

# _PPP_INFO structure


## -description


The 
<b>PPP_INFO</b> structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.


## -struct-fields




### -field nbf

A 
<a href="https://msdn.microsoft.com/376c662d-c0e1-4136-937c-47a4681c14ec">PPP_NBFCP_INFO</a> structure that contains PPP NetBEUI Framer (NBF) projection information.


### -field ip

A 
<a href="https://msdn.microsoft.com/c77f54d2-eac4-4e0a-92c5-c46d521a272d">PPP_IPCP_INFO</a> structure that contains PPP Internet Protocol (IP) projection information.


### -field ipx

A 
<a href="https://msdn.microsoft.com/6e269c4e-8014-4d59-a7dc-3314a67a4d12">PPP_IPXCP_INFO</a> structure that contains PPP Internetwork Packet Exchange (IPX) projection information.


### -field at

A 
<a href="https://msdn.microsoft.com/48d2404b-df8d-4ed0-9203-921474c88551">PPP_ATCP_INFO</a> structure that contains PPP AppleTalk projection information.


## -see-also




<a href="https://msdn.microsoft.com/5fe87e87-6199-4a96-8e76-1838e515116e">PPP_INFO_2</a>



<a href="https://msdn.microsoft.com/cc231775-83bc-45d5-8bd8-7ac4cf5f09ff">PPP_INFO_3</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

