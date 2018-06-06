---
UID: NF:bdaiface.IBDA_EthernetFilter.GetMulticastListSize
title: IBDA_EthernetFilter::GetMulticastListSize
author: windows-sdk-content
description: The GetMulticastListSize method retrieves the number of addresses currently in the list.
old-location: mstv\ibda_ethernetfilter_getmulticastlistsize.htm
old-project: mstv
ms.assetid: bc2452ca-53ad-4286-951a-c211f3f82cf3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetMulticastListSize, GetMulticastListSize method [Microsoft TV Technologies], GetMulticastListSize method [Microsoft TV Technologies],IBDA_EthernetFilter interface, IBDA_EthernetFilter interface [Microsoft TV Technologies],GetMulticastListSize method, IBDA_EthernetFilter.GetMulticastListSize, IBDA_EthernetFilter::GetMulticastListSize, IBDA_EthernetFilterGetMulticastListSize, bdaiface/IBDA_EthernetFilter::GetMulticastListSize, mstv.ibda_ethernetfilter_getmulticastlistsize
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f4f9d6c0-0acf-416b-adb3-643ac0167d0a">IBDA_EthernetFilter Interface</a>
 

 

