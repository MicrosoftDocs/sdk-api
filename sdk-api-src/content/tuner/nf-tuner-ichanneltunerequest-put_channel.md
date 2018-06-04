---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

