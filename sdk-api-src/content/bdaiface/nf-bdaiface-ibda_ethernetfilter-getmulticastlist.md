---
UID: NF:bdaiface.IBDA_EthernetFilter.GetMulticastList
title: IBDA_EthernetFilter::GetMulticastList
author: windows-sdk-content
description: The GetMulticastList method retrieves the list of multicast addresses on the Network Provider.
old-location: mstv\ibda_ethernetfilter_getmulticastlist.htm
tech.root: MSTV
ms.assetid: 65ad05c7-eb0e-450e-9bec-d46738f65dcd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMulticastList, GetMulticastList method [Microsoft TV Technologies], GetMulticastList method [Microsoft TV Technologies],IBDA_EthernetFilter interface, IBDA_EthernetFilter interface [Microsoft TV Technologies],GetMulticastList method, IBDA_EthernetFilter.GetMulticastList, IBDA_EthernetFilter::GetMulticastList, IBDA_EthernetFilterGetMulticastList, bdaiface/IBDA_EthernetFilter::GetMulticastList, mstv.ibda_ethernetfilter_getmulticastlist
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
 - IBDA_EthernetFilter.GetMulticastList
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
- IBDA_EthernetFilter.GetMulticastList
: 
---

# IBDA_EthernetFilter::GetMulticastList


## -description



The <b>GetMulticastList</b> method retrieves the list of multicast addresses on the Network Provider.




## -parameters




### -param pulcbAddresses

TBD


### -param pAddressList [out]

Pointer that receives an array of addresses whose size in bytes is equal to <i>ulcbAddresses</i>. See Remarks.


#### - ulcbAddresses [in, out]

On input, specifies the maximum number of addresses to retrieve, multiplied by the number of bytes per address. On output, receives the actual number of bytes retrieved.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The declaration of <i>pAddressList</i> is not COM compliant. As a workaround, the client should allocate the <i>pAddressList</i> buffer. The buffer should be the same size as advertised in the <i>pulcbAddresses</i> parameter. The network provider will just fill in the buffer allocated by the caller.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693329(v=VS.85).aspx">IBDA_EthernetFilter Interface</a>
 

 

