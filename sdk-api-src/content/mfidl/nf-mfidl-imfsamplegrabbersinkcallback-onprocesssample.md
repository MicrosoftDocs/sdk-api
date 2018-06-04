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

# IMFSampleGrabberSinkCallback::OnProcessSample


## -description



Called when the sample-grabber sink receives a new media sample.




## -parameters




### -param guidMajorMediaType [in]

The major type that specifies the format of the data. For a list of possible values, see <a href="https://msdn.microsoft.com/1cca3539-a920-4938-93b9-ae41e1c0a287">Major Media Types</a>.
          


### -param dwSampleFlags [in]


            Reserved.
          


### -param llSampleTime [in]

The presentation time for this sample, in 100-nanosecond units.
          If the sample does not have a presentation time, the value of this parameter is <b>_I64_MAX</b>.


### -param llSampleDuration [in]

The duration of the sample, in 100-nanosecond units.
          If the sample does not have a duration, the value of this parameter is <b>_I64_MAX</b>.


### -param pSampleBuffer [in]


            A pointer to a buffer that contains the sample data.
          


### -param dwSampleSize [in]


            Size of the <i>pSampleBuffer</i> buffer, in bytes.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you use the sample-grabber sink in a playback topology, this method should return quickly, or it might interfere with playback. Do not block the thread, wait on events, or perform other lengthy operations inside this method.




## -see-also




<a href="https://msdn.microsoft.com/6635823c-f532-4012-ad3c-382491b61671">IMFSampleGrabberSinkCallback</a>
 

 

