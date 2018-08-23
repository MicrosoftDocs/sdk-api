---
UID: NF:bdaiface.IBDA_EthernetFilter.GetMulticastListSize
title: IBDA_EthernetFilter::GetMulticastListSize
author: windows-sdk-content
description: The GetMulticastListSize method retrieves the number of addresses currently in the list.
old-location: mstv\ibda_ethernetfilter_getmulticastlistsize.htm
old-project: mstv
ms.assetid: bc2452ca-53ad-4286-951a-c211f3f82cf3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetMulticastListSize, GetMulticastListSize method [Microsoft TV Technologies], GetMulticastListSize method [Microsoft TV Technologies],IBDA_EthernetFilter interface, IBDA_EthernetFilter interface [Microsoft TV Technologies],GetMulticastListSize method, IBDA_EthernetFilter.GetMulticastListSize, IBDA_EthernetFilter::GetMulticastListSize, IBDA_EthernetFilterGetMulticastListSize, bdaiface/IBDA_EthernetFilter::GetMulticastListSize, mstv.ibda_ethernetfilter_getmulticastlistsize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
 - IBDA_EthernetFilter.GetMulticastListSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_EthernetFilter::GetMulticastListSize


## -description



The <b>GetMulticastListSize</b> method retrieves the number of addresses currently in the list.




## -parameters




### -param pulcbAddresses [out]

Pointer that receives the number of addresses currently in the Network Provider's list.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Addresses in the address list are byte aligned in Network order. <i>UlcbAddresses</i> will always be an integer multiple of the size of an Ethernet address.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693329(v=VS.85).aspx">IBDA_EthernetFilter Interface</a>
 

 

