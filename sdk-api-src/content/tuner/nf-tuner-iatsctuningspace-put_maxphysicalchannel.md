---
UID: NF:tuner.IATSCTuningSpace.put_MaxPhysicalChannel
title: IATSCTuningSpace::put_MaxPhysicalChannel
author: windows-driver-content
description: The put_MaxPhysicalChannel method sets the highest physical channel number for this tuning space.
old-location: mstv\iatsctuningspace_put_maxphysicalchannel.htm
old-project: mstv
ms.assetid: 842d2c13-eef2-42d9-9642-50ec2aafb760
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],put_MaxPhysicalChannel method, IATSCTuningSpace.put_MaxPhysicalChannel, IATSCTuningSpace::put_MaxPhysicalChannel, IATSCTuningSpaceput_MaxPhysicalChannel, mstv.iatsctuningspace_put_maxphysicalchannel, put_MaxPhysicalChannel, put_MaxPhysicalChannel method [Microsoft TV Technologies], put_MaxPhysicalChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, tuner/IATSCTuningSpace::put_MaxPhysicalChannel
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
-	IATSCTuningSpace.put_MaxPhysicalChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCTuningSpace::put_MaxPhysicalChannel


## -description



The <b>put_MaxPhysicalChannel</b> method sets the highest physical channel number for this tuning space.




## -parameters




### -param NewMaxPhysicalChannelVal [in]

Variable of type <b>long</b> that specifies the highest physical channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace Interface</a>



<a href="https://msdn.microsoft.com/67a08647-a2b5-43b2-b5d2-3917beb6dd27">IChannelTuneRequest::put_Channel</a>
 

 

