---
UID: NF:tuner.IChannelTuneRequest.get_Channel
title: IChannelTuneRequest::get_Channel
author: windows-driver-content
description: The get_Channel method gets the channel to be tuned.
old-location: mstv\ichanneltunerequest_get_channel.htm
old-project: mstv
ms.assetid: 1a529416-9b7a-41f4-961a-741b1a581d5f
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IChannelTuneRequest interface [Microsoft TV Technologies],get_Channel method, IChannelTuneRequest.get_Channel, IChannelTuneRequest::get_Channel, IChannelTuneRequestget_Channel, get_Channel, get_Channel method [Microsoft TV Technologies], get_Channel method [Microsoft TV Technologies],IChannelTuneRequest interface, mstv.ichanneltunerequest_get_channel, tuner/IChannelTuneRequest::get_Channel
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
-	IChannelTuneRequest.get_Channel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IChannelTuneRequest::get_Channel


## -description



        The <b>get_Channel</b> method gets the channel to be tuned.
      


## -parameters




### -param Channel






#### - pChannel [out]


            Pointer to a variable of type <b>long</b> that receives the current channel.
          


## -returns




            Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.
          




## -see-also




<a href="https://msdn.microsoft.com/cdb65c1a-bd86-4dc8-a72f-c08e36999880">IChannelTuneRequest Interface</a>
 

 

