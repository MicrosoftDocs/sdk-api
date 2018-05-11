---
UID: NF:tuner.IAnalogTVTuningSpace.get_MinChannel
title: IAnalogTVTuningSpace::get_MinChannel
author: windows-driver-content
description: The get_MinChannel method gets the lowest channel number for this tuning space.
old-location: mstv\ianalogtvtuningspace_get_minchannel.htm
old-project: mstv
ms.assetid: 94c3136f-6d9e-4396-9bbf-828669d57724
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],get_MinChannel method, IAnalogTVTuningSpace.get_MinChannel, IAnalogTVTuningSpace::get_MinChannel, IAnalogTVTuningSpaceget_MinChannel, get_MinChannel, get_MinChannel method [Microsoft TV Technologies], get_MinChannel method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, mstv.ianalogtvtuningspace_get_minchannel, tuner/IAnalogTVTuningSpace::get_MinChannel
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
-	IAnalogTVTuningSpace.get_MinChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogTVTuningSpace::get_MinChannel


## -description



The <b>get_MinChannel</b> method gets the lowest channel number for this tuning space.




## -parameters




### -param MinChannelVal






#### - pMinChannelVal [out]

Receives the lowest channel.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



An NTSC tuning space connected to an antenna will return a value of 2.




## -see-also




<a href="https://msdn.microsoft.com/2b531f09-bf2e-4eb2-abcf-60f64cbee17b">IAnalogTVTuningSpace Interface</a>
 

 

