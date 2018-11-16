---
UID: NF:bdaiface.IBDA_IPV6Filter.GetMulticastList
title: IBDA_IPV6Filter::GetMulticastList
author: windows-sdk-content
description: The GetMulticastList method retrieves the list of multicast addresses on the Network Provider.
old-location: mstv\ibda_ipv6filter_getmulticastlist.htm
tech.root: mstv
ms.assetid: 545c6bcb-f96c-47d7-ac33-92da016dbabf
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetMulticastList, GetMulticastList method [Microsoft TV Technologies], GetMulticastList method [Microsoft TV Technologies],IBDA_IPV6Filter interface, IBDA_IPV6Filter interface [Microsoft TV Technologies],GetMulticastList method, IBDA_IPV6Filter.GetMulticastList, IBDA_IPV6Filter::GetMulticastList, IBDA_IPV6FilterGetMulticastList, bdaiface/IBDA_IPV6Filter::GetMulticastList, mstv.ibda_ipv6filter_getmulticastlist
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
 - IBDA_IPV6Filter.GetMulticastList
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
- IBDA_IPV6Filter.GetMulticastList
: 
---

# IBDA_IPV6Filter::GetMulticastList


## -description



The <b>GetMulticastList</b> method retrieves the list of multicast addresses on the Network Provider.




## -parameters




### -param pulcbAddresses [in, out]

On input, specifies the maximum number of addresses to retrieve, multiplied by the number of bytes per address. On output, receives the actual number of bytes retrieved.


### -param pAddressList [out]

Pointer that receives an array of addresses whose size in bytes is equal to <i>ulcbAddresses</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The declaration of <i>pAddressList</i> is not COM compliant. As a workaround, the client should allocate the <i>pAddressList</i> buffer. The buffer should be the same size as advertised in the <i>pulcbAddresses</i> parameter. The network provider will just fill in the buffer allocated by the caller.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3db86e21-6d05-4b7f-be83-a3fa506a0e3b">IBDA_IPV4Filter Interface</a>
 

 

