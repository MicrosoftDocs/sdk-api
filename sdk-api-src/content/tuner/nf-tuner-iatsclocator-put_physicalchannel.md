---
UID: NF:tuner.IATSCLocator.put_PhysicalChannel
title: IATSCLocator::put_PhysicalChannel method
author: windows-driver-content
description: The put_PhysicalChannel method sets the physical channel.
old-location: mstv\iatsclocator_put_physicalchannel.htm
old-project: mstv
ms.assetid: 0699e4ef-7ebb-4515-9894-1592f07607ed
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IATSCLocator, IATSCLocator interface [Microsoft TV Technologies], put_PhysicalChannel method, IATSCLocator::put_PhysicalChannel, IATSCLocatorput_PhysicalChannel, mstv.iatsclocator_put_physicalchannel, put_PhysicalChannel method [Microsoft TV Technologies], put_PhysicalChannel method [Microsoft TV Technologies], IATSCLocator interface, put_PhysicalChannel,IATSCLocator.put_PhysicalChannel, tuner/IATSCLocator::put_PhysicalChannel
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
-	IATSCLocator.put_PhysicalChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCLocator::put_PhysicalChannel method


## -description



The <b>put_PhysicalChannel</b> method sets the physical channel.




## -parameters




### -param PhysicalChannel [in]

The physical channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This is a required property. A tuner cannot locate an ATSC transmission source without it.




## -see-also




<a href="https://msdn.microsoft.com/8ca7d50f-e7cc-4938-a2ed-fce5278b73fd">IATSCLocator Interface</a>
 

 

