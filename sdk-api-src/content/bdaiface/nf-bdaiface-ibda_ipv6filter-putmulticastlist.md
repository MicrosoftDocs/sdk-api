---
UID: NF:bdaiface.IBDA_IPV6Filter.PutMulticastList
title: IBDA_IPV6Filter::PutMulticastList
author: windows-sdk-content
description: The PutMulticastList method specifies the parameters of the multicast list.
old-location: mstv\ibda_ipv6filter_putmulticastlist.htm
tech.root: mstv
ms.assetid: a0e77856-5a7d-4312-a4f1-69d186c90855
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_IPV6Filter interface [Microsoft TV Technologies],PutMulticastList method, IBDA_IPV6Filter.PutMulticastList, IBDA_IPV6Filter::PutMulticastList, IBDA_IPV6FilterPutMulticastList, PutMulticastList, PutMulticastList method [Microsoft TV Technologies], PutMulticastList method [Microsoft TV Technologies],IBDA_IPV6Filter interface, bdaiface/IBDA_IPV6Filter::PutMulticastList, mstv.ibda_ipv6filter_putmulticastlist
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
 - IBDA_IPV6Filter.PutMulticastList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_IPV6Filter::PutMulticastList


## -description



The <b>PutMulticastList</b> method specifies the parameters of the multicast list.




## -parameters




### -param ulcbAddresses [in]

Specifies the number of addresses in the list, multiplied by the number of bytes per address.


### -param pAddressList [in]

Pointer to an array of addresses whose size in bytes is equal to <i>ulcbAddresses</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b506d382-c56d-4c5b-ad57-e186173ea9a8">IBDA_IPV6Filter Interface</a>
 

 

