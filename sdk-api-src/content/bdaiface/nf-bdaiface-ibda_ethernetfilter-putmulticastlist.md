---
UID: NF:bdaiface.IBDA_EthernetFilter.PutMulticastList
title: IBDA_EthernetFilter::PutMulticastList
author: windows-sdk-content
description: The PutMulticastList method sets the list of multicast addresses on the Network Provider.
old-location: mstv\ibda_ethernetfilter_putmulticastlist.htm
old-project: mstv
ms.assetid: 0398dc58-07be-40cd-95af-62b29a191d3c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_EthernetFilter interface [Microsoft TV Technologies],PutMulticastList method, IBDA_EthernetFilter.PutMulticastList, IBDA_EthernetFilter::PutMulticastList, IBDA_EthernetFilterPutMulticastList, PutMulticastList, PutMulticastList method [Microsoft TV Technologies], PutMulticastList method [Microsoft TV Technologies],IBDA_EthernetFilter interface, bdaiface/IBDA_EthernetFilter::PutMulticastList, mstv.ibda_ethernetfilter_putmulticastlist
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
 - IBDA_EthernetFilter.PutMulticastList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_EthernetFilter::PutMulticastList


## -description



The <b>PutMulticastList</b> method sets the list of multicast addresses on the Network Provider.




## -parameters




### -param ulcbAddresses [in]

Specifies the number of addresses in the list, multiplied by the number of bytes per address.


### -param pAddressList [in]

Pointer to an array of addresses whose size in bytes is equal to <i>ulcbAddresses</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f4f9d6c0-0acf-416b-adb3-643ac0167d0a">IBDA_EthernetFilter Interface</a>
 

 

