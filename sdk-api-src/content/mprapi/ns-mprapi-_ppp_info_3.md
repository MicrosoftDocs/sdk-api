---
UID: NS:mprapi._PPP_INFO_3
title: "_PPP_INFO_3"
author: windows-sdk-content
description: The PPP_INFO_3 structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.
old-location: rras\ppp_info_3.htm
tech.root: rras
ms.assetid: cc231775-83bc-45d5-8bd8-7ac4cf5f09ff
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: PPP_INFO_3, PPP_INFO_3 structure [RAS], _PPP_INFO_3, mprapi/PPP_INFO_3, rras.ppp_info_3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mprapi.h
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
 - Mprapi.h
api_name:
 - PPP_INFO_3
product: Windows
targetos: Windows
req.typenames: PPP_INFO_3
req.redist: 
---

# _PPP_INFO_3 structure


## -description


The 
<b>PPP_INFO_3</b> structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.


## -struct-fields




### -field nbf

A 
<a href="https://msdn.microsoft.com/376c662d-c0e1-4136-937c-47a4681c14ec">PPP_NBFCP_INFO</a> structure that contains PPP NetBEUI Framer (NBF) projection information.


### -field ip

A 
<a href="https://msdn.microsoft.com/e12cde70-51af-484b-a700-f3976a3abc4a">PPP_IPCP_INFO2</a> structure that contains PPP Internet Protocol (IP) projection information.


### -field ipv6

A 
<a href="https://msdn.microsoft.com/fb77a15d-a513-456d-9d55-258b93fe8db5">PPP_IPV6_CP_INFO</a> structure that contains IPv6 control protocol projection information.


### -field ccp

A 
<a href="https://msdn.microsoft.com/d50493c4-8a18-4cab-8973-a752f3f7f6c2">PPP_CCP_INFO</a> structure that contains Compression Control Protocol (CCP) projection information.


### -field lcp

A 
<a href="https://msdn.microsoft.com/b6158047-6337-483f-9a90-74d578831772">PPP_LCP_INFO</a> structure that contains PPP Link Control Protocol (LCP) projection information.


## -see-also




<a href="https://msdn.microsoft.com/39692a38-ab40-43da-a704-8c206be72ceb">PPP_INFO</a>



<a href="https://msdn.microsoft.com/5fe87e87-6199-4a96-8e76-1838e515116e">PPP_INFO_2</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

