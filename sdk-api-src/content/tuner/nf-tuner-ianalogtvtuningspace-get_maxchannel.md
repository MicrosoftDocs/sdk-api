---
UID: NF:tuner.IAnalogTVTuningSpace.get_MaxChannel
title: IAnalogTVTuningSpace::get_MaxChannel method
author: windows-driver-content
description: The get_MaxChannel method gets the highest channel number for this tuning space.
old-location: mstv\ianalogtvtuningspace_get_maxchannel.htm
old-project: mstv
ms.assetid: e6ac3789-1989-4331-ad00-6720f4503bb7
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAnalogTVTuningSpace, IAnalogTVTuningSpace interface [Microsoft TV Technologies], get_MaxChannel method, IAnalogTVTuningSpace::get_MaxChannel, IAnalogTVTuningSpaceget_MaxChannel, get_MaxChannel method [Microsoft TV Technologies], get_MaxChannel method [Microsoft TV Technologies], IAnalogTVTuningSpace interface, get_MaxChannel,IAnalogTVTuningSpace.get_MaxChannel, mstv.ianalogtvtuningspace_get_maxchannel, tuner/IAnalogTVTuningSpace::get_MaxChannel
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
-	IAnalogTVTuningSpace.get_MaxChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogTVTuningSpace::get_MaxChannel method


## -description



The <b>get_MaxChannel</b> method gets the highest channel number for this tuning space.




## -parameters




### -param MaxChannelVal






#### - pMaxChannelVal [out]

Receives the highest channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



For example, an NTSC tuning space connected to an antenna would return 69.




## -see-also




<a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace Interface</a>
 

 

