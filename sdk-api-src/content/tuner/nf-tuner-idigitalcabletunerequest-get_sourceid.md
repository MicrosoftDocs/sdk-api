---
UID: NF:tuner.IDigitalCableTuneRequest.get_SourceID
title: IDigitalCableTuneRequest::get_SourceID
author: windows-sdk-content
description: The get_SourceID method retrieves the source identifier, which maps to a physical channel.
old-location: mstv\idigitalcabletunerequest_get_sourceid.htm
old-project: mstv
ms.assetid: 3767a8b4-f318-4242-9b30-f1293b3f7091
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDigitalCableTuneRequest interface [Microsoft TV Technologies],get_SourceID method, IDigitalCableTuneRequest.get_SourceID, IDigitalCableTuneRequest::get_SourceID, IDigitalCableTuneRequestget_SourceID, get_SourceID, get_SourceID method [Microsoft TV Technologies], get_SourceID method [Microsoft TV Technologies],IDigitalCableTuneRequest interface, mstv.idigitalcabletunerequest_get_sourceid, tuner/IDigitalCableTuneRequest::get_SourceID
ms.prod: windows
ms.technology: windows-sdk
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
 - IDigitalCableTuneRequest.get_SourceID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDigitalCableTuneRequest::get_SourceID


## -description



The <b>get_SourceID</b> method retrieves the source identifier, which maps to a physical channel.




## -parameters




### -param pSourceID [out]

Receives the source identifier. If the value received is BDA_UNDEFINED_CHANNEL, the source identifier is not used.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/75c3c80f-2f02-4cb7-a9e0-aad4076793e4">IDigitalCableTuneRequest Interface</a>
 

 

