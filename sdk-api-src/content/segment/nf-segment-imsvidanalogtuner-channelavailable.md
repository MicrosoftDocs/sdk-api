---
UID: NF:segment.IMSVidAnalogTuner.ChannelAvailable
title: IMSVidAnalogTuner::ChannelAvailable
author: windows-sdk-content
description: The ChannelAvailable method queries whether a specified channel is available for viewing.
old-location: mstv\imsvidanalogtuner_channelavailable.htm
tech.root: MSTV
ms.assetid: 67533d80-6026-434f-a20f-ded3c119d318
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ChannelAvailable, ChannelAvailable method [Microsoft TV Technologies], ChannelAvailable method [Microsoft TV Technologies],IMSVidAnalogTuner interface, IMSVidAnalogTuner interface [Microsoft TV Technologies],ChannelAvailable method, IMSVidAnalogTuner.ChannelAvailable, IMSVidAnalogTuner::ChannelAvailable, IMSVidAnalogTunerChannelAvailable, mstv.imsvidanalogtuner_channelavailable, segment/IMSVidAnalogTuner::ChannelAvailable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidAnalogTuner.ChannelAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidAnalogTuner::ChannelAvailable


## -description


The <b>ChannelAvailable</b> method queries whether a specified channel is available for viewing.

This method is currently not supported.


## -parameters




### -param nChannel [in]

Integer containing the channel.


### -param SignalStrength

TBD


### -param fSignalPresent

TBD




#### - pSignalStrength [in, out]

Pointer to a <b>long</b> value that specifies the signal strength.


#### - pfSignalPresent [out]

Receives a <b>VARIANT_BOOL</b> that indicates whether a signal is present.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/64a89038-4df1-4e30-8952-6dc039a2e18b">IAMTuner::SignalPresent</a>



<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner Interface</a>
 

 

