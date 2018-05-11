---
UID: NF:bdaiface.IBDA_EthernetFilter.GetMulticastMode
title: IBDA_EthernetFilter::GetMulticastMode
author: windows-driver-content
description: The GetMulticastMode method retrieves the multicast mode.
old-location: mstv\ibda_ethernetfilter_getmulticastmode.htm
old-project: mstv
ms.assetid: 8a0a5dbb-642a-458b-a5b2-80e993ab61ca
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetMulticastMode, GetMulticastMode method [Microsoft TV Technologies], GetMulticastMode method [Microsoft TV Technologies],IBDA_EthernetFilter interface, IBDA_EthernetFilter interface [Microsoft TV Technologies],GetMulticastMode method, IBDA_EthernetFilter.GetMulticastMode, IBDA_EthernetFilter::GetMulticastMode, IBDA_EthernetFilterGetMulticastMode, bdaiface/IBDA_EthernetFilter::GetMulticastMode, mstv.ibda_ethernetfilter_getmulticastmode
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_EthernetFilter.GetMulticastMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_EthernetFilter::GetMulticastMode


## -description



The <b>GetMulticastMode</b> method retrieves the multicast mode.




## -parameters




### -param pulModeMask [out]

Pointer that receives the multicast mode.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



See the Windows DDK for possible values.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f4f9d6c0-0acf-416b-adb3-643ac0167d0a">IBDA_EthernetFilter Interface</a>



<a href="https://msdn.microsoft.com/01694aba-6b43-46da-a35c-7f3f5befecad">PutMulticastMode</a>
 

 

