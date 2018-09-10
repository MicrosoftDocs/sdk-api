---
UID: NF:tuner.IATSCTuningSpace.put_MinPhysicalChannel
title: IATSCTuningSpace::put_MinPhysicalChannel
author: windows-sdk-content
description: The put_MinPhysicalChannel method sets the lowest physical channel number for this tuning space.
old-location: mstv\iatsctuningspace_put_minphysicalchannel.htm
tech.root: mstv
ms.assetid: 57192470-8013-4812-af95-cb6ce92bea83
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IATSCTuningSpace interface [Microsoft TV Technologies],put_MinPhysicalChannel method, IATSCTuningSpace.put_MinPhysicalChannel, IATSCTuningSpace::put_MinPhysicalChannel, IATSCTuningSpaceput_MinPhysicalChannel, mstv.iatsctuningspace_put_minphysicalchannel, put_MinPhysicalChannel, put_MinPhysicalChannel method [Microsoft TV Technologies], put_MinPhysicalChannel method [Microsoft TV Technologies],IATSCTuningSpace interface, tuner/IATSCTuningSpace::put_MinPhysicalChannel
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IATSCTuningSpace.put_MinPhysicalChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSCTuningSpace::put_MinPhysicalChannel


## -description



The <b>put_MinPhysicalChannel</b> method sets the lowest physical channel number for this tuning space.




## -parameters




### -param NewMinPhysicalChannelVal [in]

Variable of type <b>long</b> that specifies the lowest physical channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace Interface</a>



<a href="https://msdn.microsoft.com/67a08647-a2b5-43b2-b5d2-3917beb6dd27">IChannelTuneRequest::put_Channel</a>
 

 

