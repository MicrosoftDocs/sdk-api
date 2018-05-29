---
UID: NF:tuner.IATSCChannelTuneRequest.get_MinorChannel
title: IATSCChannelTuneRequest::get_MinorChannel
author: windows-sdk-content
description: The get_MinorChannel method gets the current minor channel.
old-location: mstv\iatscchanneltunerequest_get_minorchannel.htm
old-project: mstv
ms.assetid: 2b8aa006-faba-472b-836b-0ff1ae134232
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IATSCChannelTuneRequest interface [Microsoft TV Technologies],get_MinorChannel method, IATSCChannelTuneRequest.get_MinorChannel, IATSCChannelTuneRequest::get_MinorChannel, IATSCChannelTuneRequestget_MinorChannel, get_MinorChannel, get_MinorChannel method [Microsoft TV Technologies], get_MinorChannel method [Microsoft TV Technologies],IATSCChannelTuneRequest interface, mstv.iatscchanneltunerequest_get_minorchannel, tuner/IATSCChannelTuneRequest::get_MinorChannel
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IATSCChannelTuneRequest.get_MinorChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCChannelTuneRequest::get_MinorChannel


## -description



The <b>get_MinorChannel</b> method gets the current minor channel.




## -parameters




### -param MinorChannel






#### - pMinorChannel [out]

Receives the current minor channel. If the value received is -1, the tuner should tune to the first valid minor channel it finds.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/9b55e181-ae03-473c-a85a-f169744d911d">IATSCChannelTuneRequest Interface</a>
 

 

