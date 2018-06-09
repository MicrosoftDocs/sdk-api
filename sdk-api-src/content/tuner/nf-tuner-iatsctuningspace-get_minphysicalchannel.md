---
UID: NF:tuner.IATSCTuningSpace.get_MinPhysicalChannel
title: IATSCTuningSpace::get_MinPhysicalChannel
author: windows-sdk-content
description: The get_MinPhysicalChannel method sets the lowest physical channel number for this tuning space.
old-location: mstv\iatsctuningspace_get_minphysicalchannel.htm
old-project: mstv
ms.assetid: 1b85331a-d99f-4cb6-8440-1b51fa697ade
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],get_MinPhysicalChannel method, IATSCTuningSpace.get_MinPhysicalChannel, IATSCTuningSpace::get_MinPhysicalChannel, IATSCTuningSpaceget_MinPhysicalChannel, get_MinPhysicalChannel, get_MinPhysicalChannel method [Microsoft TV Technologies], get_MinPhysicalChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, mstv.iatsctuningspace_get_minphysicalchannel, tuner/IATSCTuningSpace::get_MinPhysicalChannel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IATSCTuningSpace.get_MinPhysicalChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCTuningSpace::get_MinPhysicalChannel


## -description



The <b>get_MinPhysicalChannel</b> method sets the lowest physical channel number for this tuning space.




## -parameters




### -param MinPhysicalChannelVal






#### - pMinPhysicalChannelVal [out]

Receives the lowest physical channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace Interface</a>



<a href="https://msdn.microsoft.com/67a08647-a2b5-43b2-b5d2-3917beb6dd27">IChannelTuneRequest::put_Channel</a>
 

 

