---
UID: NS:mprapi._PPP_IPV6_CP_INFO
title: "_PPP_IPV6_CP_INFO"
author: windows-sdk-content
description: Contains the result of an IPv6 control protocol negotiation.
old-location: rras\ppp_ipv6cp_info.htm
old-project: RRAS
ms.assetid: fb77a15d-a513-456d-9d55-258b93fe8db5
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: PPPP_IPV6_CP_INFO, PPPP_IPV6_CP_INFO structure pointer [RAS], PPP_IPV6_CP_INFO, PPP_IPV6_CP_INFO structure [RAS], _PPP_IPV6_CP_INFO, mprapi/PPPP_IPV6_CP_INFO, mprapi/PPP_IPV6_CP_INFO, rras.ppp_ipv6cp_info
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
req.typenames: PPP_IPV6_CP_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mprapi.h
api_name:
-	PPP_IPV6_CP_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _PPP_IPV6_CP_INFO structure


## -description


The <b>PPP_IPV6_CP_INFO</b> structure contains the result of an IPv6 control protocol negotiation.


## -struct-fields




### -field dwVersion

The version of the <b>PPP_IPV6_CP_INFO</b> structure used. 


### -field dwSize

The size, in bytes, of this <b>PPP_IPV6_CP_INFO</b> structure.


### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.


### -field bInterfaceIdentifier

Specifies the 64 bit interface identifier of the IPv6 server interface.


### -field bRemoteInterfaceIdentifier

Specifies the 64 bit interface identifier of the IPv6 client interface.


### -field dwOptions

Reserved. Must be set to 0.


### -field dwRemoteOptions

Reserved. Must be set to 0.


### -field bPrefix

Specifies the address prefix of the IPv6 client interface.


### -field dwPrefixLength

The length, in bits, of the address prefix.


## -see-also




<a href="https://msdn.microsoft.com/39692a38-ab40-43da-a704-8c206be72ceb">PPP_INFO</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

