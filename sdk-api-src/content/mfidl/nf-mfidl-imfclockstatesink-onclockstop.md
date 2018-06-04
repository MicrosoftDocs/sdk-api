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

# IMFClockStateSink::OnClockStop


## -description



          Called when the presentation clock stops.
        


## -parameters




### -param hnsSystemTime






#### - hnssSystemTime [in]


            The system time when the clock stopped, in 100-nanosecond units.
          


## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SINK_ALREADYSTOPPED</b></dt>
</dl>
</td>
<td width="60%">
Deprecated. Do not use this error code.

</td>
</tr>
</table>
 




## -remarks




        When the presentation clock's <a href="https://msdn.microsoft.com/54377d65-2af7-410d-b8cf-45f467527a45">IMFPresentationClock::Stop</a> method is called, the clock notifies the presentation time source by calling the presentation time source's <b>OnClockStop</b> method. This call occurs synchronously within the <b>Stop</b> method. If the time source returns an error from <b>OnClockStop</b>, the presentation clock's <b>Stop</b> method returns an error and the state change does not take place.
      


        For any object that is not the presentation time source, the <b>OnClockStop</b> method is called asynchronously, after the state change is completed. 

If an object is already stopped, it should return <b>S_OK</b> from <b>OnClockStop</b>. It should not return an error code. 

<div class="alert"><b>Note</b>  Although the header file mferror.h defines an error code named <b>MF_E_SINK_ALREADYSTOPPED</b>, it should not be returned in this situation.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

