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

# IMFMediaSinkPreroll::NotifyPreroll


## -description



          Notifies the media sink that the presentation clock is about to start.
        


## -parameters




### -param hnsUpcomingStartTime [in]


            The upcoming start time for the presentation clock, in 100-nanosecond units. This time is the same value that will be given to the <a href="https://msdn.microsoft.com/ba5986d1-9c94-4747-a221-43d0583f1fed">IMFPresentationClock::Start</a> method when the presentation clock is started.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        After this method is called, the media sink sends any number of <a href="https://msdn.microsoft.com/35020a15-942f-4dd0-9ca4-815affdacecf">MEStreamSinkRequestSample</a> events to request samples, until is has enough preroll data. When it has enough preroll data, the media sink sends an <a href="https://msdn.microsoft.com/1ecb1805-73ce-4741-b969-6eb88982ee26">MEStreamSinkPrerolled</a> event. This event signals that the client can start the presentation clock.
      


        During preroll, the media sink can prepare the samples that it receives, so that they are ready to be rendered. It does not actually render any samples until the clock starts.
      




## -see-also




<a href="https://msdn.microsoft.com/7cc93751-4477-4649-b09e-53f519fb1acb">IMFMediaSinkPreroll</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

