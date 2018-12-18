---
UID: NF:tuner.IDigitalCableTuneRequest.get_MajorChannel
title: IDigitalCableTuneRequest::get_MajorChannel
author: windows-sdk-content
description: The get_MajorChannel method retrieves the major channel number.
old-location: mstv\idigitalcabletunerequest_get_majorchannel.htm
tech.root: mstv
ms.assetid: f8c59c66-1c86-4cfd-b295-ac1d1a75af17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDigitalCableTuneRequest interface [Microsoft TV Technologies],get_MajorChannel method, IDigitalCableTuneRequest.get_MajorChannel, IDigitalCableTuneRequest::get_MajorChannel, IDigitalCableTuneRequestget_MajorChannel, get_MajorChannel, get_MajorChannel method [Microsoft TV Technologies], get_MajorChannel method [Microsoft TV Technologies],IDigitalCableTuneRequest interface, mstv.idigitalcabletunerequest_get_majorchannel, tuner/IDigitalCableTuneRequest::get_MajorChannel
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IDigitalCableTuneRequest.get_MajorChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDigitalCableTuneRequest::get_MajorChannel


## -description



The <b>get_MajorChannel</b> method retrieves the major channel number.




## -parameters




### -param pMajorChannel [out]

Receives the major channel number. If the value received is BDA_UNDEFINED_CHANNEL, the major channel number is not used.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/75c3c80f-2f02-4cb7-a9e0-aad4076793e4">IDigitalCableTuneRequest Interface</a>
 

 

