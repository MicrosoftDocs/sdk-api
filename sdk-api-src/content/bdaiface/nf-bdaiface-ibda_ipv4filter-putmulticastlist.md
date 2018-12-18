---
UID: NF:bdaiface.IBDA_IPV4Filter.PutMulticastList
title: IBDA_IPV4Filter::PutMulticastList
author: windows-sdk-content
description: The PutMulticastList method sets the list of multicast addresses on the Network Provider.
old-location: mstv\ibda_ipv4filter_putmulticastlist.htm
tech.root: mstv
ms.assetid: 06b93c7d-662e-408b-94e3-137287160898
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_IPV4Filter interface [Microsoft TV Technologies],PutMulticastList method, IBDA_IPV4Filter.PutMulticastList, IBDA_IPV4Filter::PutMulticastList, IBDA_IPV4FilterPutMulticastList, PutMulticastList, PutMulticastList method [Microsoft TV Technologies], PutMulticastList method [Microsoft TV Technologies],IBDA_IPV4Filter interface, bdaiface/IBDA_IPV4Filter::PutMulticastList, mstv.ibda_ipv4filter_putmulticastlist
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
 - IBDA_IPV4Filter.PutMulticastList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_IPV4Filter::PutMulticastList


## -description



The <b>PutMulticastList</b> method sets the list of multicast addresses on the Network Provider.




## -parameters




### -param ulcbAddresses [in]

Specifies the number of addresses in the list, times the number of bytes per address.


### -param pAddressList [in]

Pointer that receives an array of addresses whose size in bytes is equal to <i>ulcbAddresses</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693382(v=VS.85).aspx">IBDA_IPV4Filter Interface</a>
 

 

