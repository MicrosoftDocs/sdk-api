---
UID: NF:mfidl.IMFPresentationClock.GetTime
title: IMFPresentationClock::GetTime
author: windows-driver-content
description: Retrieves the latest clock time.
old-location: mf\imfpresentationclock_gettime.htm
old-project: medfound
ms.assetid: 31037b75-9fa5-48e0-a58c-a451b445147f
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 31037b75-9fa5-48e0-a58c-a451b445147f, GetTime, GetTime method [Media Foundation], GetTime method [Media Foundation],IMFPresentationClock interface, IMFPresentationClock interface [Media Foundation],GetTime method, IMFPresentationClock.GetTime, IMFPresentationClock::GetTime, mf.imfpresentationclock_gettime, mfidl/IMFPresentationClock::GetTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFPresentationClock.GetTime
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPresentationClock::GetTime


## -description



          Retrieves the latest clock time.
        


## -parameters




### -param phnsClockTime [out]


            Receives the latest clock time, in 100-nanosecond units. The time is relative to when the clock was last started.
          


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
<dt><b>MF_E_CLOCK_NO_TIME_SOURCE</b></dt>
</dl>
</td>
<td width="60%">

                The clock does not have a presentation time source. Call <a href="https://msdn.microsoft.com/170b7c8e-9d1a-4168-964a-5fd057d1e8f9">IMFPresentationClock::SetTimeSource</a>.
              

</td>
</tr>
</table>
 




## -remarks



This method does not attempt to smooth out jitter or otherwise account for any inaccuracies in the clock time.




## -see-also




<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

