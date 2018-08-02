---
UID: NF:tuner.IATSCChannelTuneRequest.put_MinorChannel
title: IATSCChannelTuneRequest::put_MinorChannel
author: windows-sdk-content
description: The put_MinorChannel method sets the minor channel to be tuned.
old-location: mstv\iatscchanneltunerequest_put_minorchannel.htm
old-project: mstv
ms.assetid: 1288d249-58de-410e-852b-233133f56da5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IATSCChannelTuneRequest interface [Microsoft TV Technologies],put_MinorChannel method, IATSCChannelTuneRequest.put_MinorChannel, IATSCChannelTuneRequest::put_MinorChannel, IATSCChannelTuneRequestput_MinorChannel, mstv.iatscchanneltunerequest_put_minorchannel, put_MinorChannel, put_MinorChannel method [Microsoft TV Technologies], put_MinorChannel method [Microsoft TV Technologies],IATSCChannelTuneRequest interface, tuner/IATSCChannelTuneRequest::put_MinorChannel
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
 - IATSCChannelTuneRequest.put_MinorChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCChannelTuneRequest::put_MinorChannel


## -description



The <b>put_MinorChannel</b> method sets the minor channel to be tuned.




## -parameters




### -param MinorChannel [in]

Specifies the minor channel. If the value is -1, the tuner tunes to the first valid minor channel it finds.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/9b55e181-ae03-473c-a85a-f169744d911d">IATSCChannelTuneRequest Interface</a>
 

 

