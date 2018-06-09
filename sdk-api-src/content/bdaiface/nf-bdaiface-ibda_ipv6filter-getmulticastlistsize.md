---
UID: NF:bdaiface.IBDA_IPV6Filter.GetMulticastListSize
title: IBDA_IPV6Filter::GetMulticastListSize
author: windows-sdk-content
description: The GetMulticastListSize method retrieves the size in bytes of the list of multicast addresses.
old-location: mstv\ibda_ipv6filter_getmulticastlistsize.htm
old-project: mstv
ms.assetid: b607774a-3c0e-49b1-881a-fd8ae2c70fb1
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetMulticastListSize, GetMulticastListSize method [Microsoft TV Technologies], GetMulticastListSize method [Microsoft TV Technologies],IBDA_IPV6Filter interface, IBDA_IPV6Filter interface [Microsoft TV Technologies],GetMulticastListSize method, IBDA_IPV6Filter.GetMulticastListSize, IBDA_IPV6Filter::GetMulticastListSize, IBDA_IPV6FilterGetMulticastListSize, bdaiface/IBDA_IPV6Filter::GetMulticastListSize, mstv.ibda_ipv6filter_getmulticastlistsize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_IPV6Filter.GetMulticastListSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_IPV6Filter::GetMulticastListSize


## -description



The <b>GetMulticastListSize</b> method retrieves the size in bytes of the list of multicast addresses.




## -parameters




### -param pulcbAddresses [in, out]

Pointer that receives the size in bytes.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is used by the <a href="https://msdn.microsoft.com/78cd6cba-3bd7-4ad4-b65d-c6b866a18d4e">BDA IP Sink</a> filter to request that a Network Provider make its best effort to tune to the stream(s) on which a list of IPv6 multicast addresses may be transmitted. Addresses in the address list are byte aligned in Network order. <i>UlcbAddresses</i> will always be an integer multiple of the size of an IPv6 address.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b506d382-c56d-4c5b-ad57-e186173ea9a8">IBDA_IPV6Filter Interface</a>
 

 

