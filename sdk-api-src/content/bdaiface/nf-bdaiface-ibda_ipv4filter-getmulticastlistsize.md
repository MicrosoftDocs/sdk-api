---
UID: NF:bdaiface.IBDA_IPV4Filter.GetMulticastListSize
title: IBDA_IPV4Filter::GetMulticastListSize
author: windows-sdk-content
description: The GetMulticastListSize method retrieves the number of addresses in the list.
old-location: mstv\ibda_ipv4filter_getmulticastlistsize.htm
tech.root: MSTV
ms.assetid: 7d31e34f-1997-40fe-9b32-a193d3017798
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMulticastListSize, GetMulticastListSize method [Microsoft TV Technologies], GetMulticastListSize method [Microsoft TV Technologies],IBDA_IPV4Filter interface, IBDA_IPV4Filter interface [Microsoft TV Technologies],GetMulticastListSize method, IBDA_IPV4Filter.GetMulticastListSize, IBDA_IPV4Filter::GetMulticastListSize, IBDA_IPV4FilterGetMulticastListSize, bdaiface/IBDA_IPV4Filter::GetMulticastListSize, mstv.ibda_ipv4filter_getmulticastlistsize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_IPV4Filter.GetMulticastListSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- IBDA_IPV4Filter.GetMulticastListSize
: 
---

# IBDA_IPV4Filter::GetMulticastListSize


## -description



The <b>GetMulticastListSize</b> method retrieves the number of addresses in the list.




## -parameters




### -param pulcbAddresses [in, out]

Pointer that receives the number of addresses multiplied by the size of an IPv4 address.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is used by an IPv4 Network Data Sink filter to request that a Network Provider make its best effort to tune to the stream(s) on which a list of IPv4 multicast addresses may be transmitted. Addresses in the address list are byte-aligned in Network order. <i>UlcbAddresses</i> will always be an integer multiple of the size of an IPv4 address.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3db86e21-6d05-4b7f-be83-a3fa506a0e3b">IBDA_IPV4Filter Interface</a>
 

 

