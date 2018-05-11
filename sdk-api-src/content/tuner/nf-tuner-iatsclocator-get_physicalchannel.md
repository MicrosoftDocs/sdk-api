---
UID: NF:tuner.IATSCLocator.get_PhysicalChannel
title: IATSCLocator::get_PhysicalChannel
author: windows-driver-content
description: The get_PhysicalChannel method retrieves the physical channel.
old-location: mstv\iatsclocator_get_physicalchannel.htm
old-project: mstv
ms.assetid: 7550bbb9-d9f7-4565-9c63-7179c0bdffa5
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IATSCLocator interface [Microsoft TV Technologies],get_PhysicalChannel method, IATSCLocator.get_PhysicalChannel, IATSCLocator::get_PhysicalChannel, IATSCLocatorget_PhysicalChannel, get_PhysicalChannel, get_PhysicalChannel method [Microsoft TV Technologies], get_PhysicalChannel method [Microsoft TV Technologies],IATSCLocator interface, mstv.iatsclocator_get_physicalchannel, tuner/IATSCLocator::get_PhysicalChannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IATSCLocator.get_PhysicalChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCLocator::get_PhysicalChannel


## -description



The <b>get_PhysicalChannel</b> method retrieves the physical channel.




## -parameters




### -param PhysicalChannel






#### - pPhysicalChannel [out]

Receives the physical channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This is a required property. A tuner cannot locate an ATSC transmission source without it.




## -see-also




<a href="https://msdn.microsoft.com/8ca7d50f-e7cc-4938-a2ed-fce5278b73fd">IATSCLocator Interface</a>
 

 

