---
UID: NF:tuner.IChannelTuneRequest.put_Channel
title: IChannelTuneRequest::put_Channel
author: windows-driver-content
description: The put_Channel method sets the channel to be tuned.
old-location: mstv\ichanneltunerequest_put_channel.htm
old-project: mstv
ms.assetid: 67a08647-a2b5-43b2-b5d2-3917beb6dd27
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IChannelTuneRequest interface [Microsoft TV Technologies],put_Channel method, IChannelTuneRequest.put_Channel, IChannelTuneRequest::put_Channel, IChannelTuneRequestput_Channel, mstv.ichanneltunerequest_put_channel, put_Channel, put_Channel method [Microsoft TV Technologies], put_Channel method [Microsoft TV Technologies],IChannelTuneRequest interface, tuner/IChannelTuneRequest::put_Channel
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
-	IChannelTuneRequest.put_Channel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IChannelTuneRequest::put_Channel


## -description



        The <b>put_Channel</b> method sets the channel to be tuned.
      


## -parameters




### -param Channel [in]


            Variable of type <b>long</b> that specifies the channel.
          


## -returns




            Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM IErrorInfo interface.
          




## -remarks




        If the value specified for <i>Channel</i> is less than the minimum channel set for the tuning space, it will "wrap around" to the maximum channel value. Likewise, if the value specified for <i>Channel</i> is greater than the maximum channel set for the tuning space, it will "wrap around" to the minimum channel value.
      




## -see-also




<a href="https://msdn.microsoft.com/cdb65c1a-bd86-4dc8-a72f-c08e36999880">IChannelTuneRequest Interface</a>
 

 

