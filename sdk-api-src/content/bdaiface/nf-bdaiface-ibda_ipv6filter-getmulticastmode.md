---
UID: NF:bdaiface.IBDA_IPV6Filter.GetMulticastMode
title: IBDA_IPV6Filter::GetMulticastMode (bdaiface.h)
author: windows-sdk-content
description: The GetMulticastMode method retrieves the mode(s) of the multicast.
old-location: mstv\ibda_ipv6filter_getmulticastmode.htm
tech.root: mstv
ms.assetid: 158e9569-b535-4744-ba12-c8a09f3e8491
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMulticastMode, GetMulticastMode method [Microsoft TV Technologies], GetMulticastMode method [Microsoft TV Technologies],IBDA_IPV6Filter interface, IBDA_IPV6Filter interface [Microsoft TV Technologies],GetMulticastMode method, IBDA_IPV6Filter.GetMulticastMode, IBDA_IPV6Filter::GetMulticastMode, IBDA_IPV6FilterGetMulticastMode, bdaiface/IBDA_IPV6Filter::GetMulticastMode, mstv.ibda_ipv6filter_getmulticastmode
ms.topic: method
f1_keywords: 
 - "bdaiface/IBDA_IPV6Filter.GetMulticastMode"
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
 - IBDA_IPV6Filter.GetMulticastMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_IPV6Filter::GetMulticastMode


## -description



The <b>GetMulticastMode</b> method retrieves the mode(s) of the multicast.




## -parameters




### -param pulModeMask [out]

Pointer that receives the mode mask.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipv6filter">IBDA_IPV6Filter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipv4filter-putmulticastmode">PutMulticastMode</a>
 

 

