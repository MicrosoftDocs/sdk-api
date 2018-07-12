---
UID: NF:mfidl.IMFClock.GetCorrelatedTime
title: IMFClock::GetCorrelatedTime
author: windows-sdk-content
description: Retrieves the last clock time that was correlated with system time.
old-location: mf\imfclock_getcorrelatedtime.htm
old-project: medfound
ms.assetid: 0a897426-d994-4b27-9f13-9b0c7c9b3a9b
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 0a897426-d994-4b27-9f13-9b0c7c9b3a9b, GetCorrelatedTime, GetCorrelatedTime method [Media Foundation], GetCorrelatedTime method [Media Foundation],IMFClock interface, IMFClock interface [Media Foundation],GetCorrelatedTime method, IMFClock.GetCorrelatedTime, IMFClock::GetCorrelatedTime, mf.imfclock_getcorrelatedtime, mfidl/IMFClock::GetCorrelatedTime
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFClock.GetCorrelatedTime
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFClock::GetCorrelatedTime


## -description



          Retrieves the last clock time that was correlated with system time.
        


## -parameters




### -param dwReserved [in]


            Reserved, must be zero.
          


### -param pllClockTime [out]


            Receives the last known clock time, in units of the clock's frequency.
          


### -param phnsSystemTime [out]


            Receives the system time that corresponds to the clock time returned in <i>pllClockTime</i>, in 100-nanosecond units.
          


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

                The clock does not have a time source.
              

</td>
</tr>
</table>
 




## -remarks



At some fixed interval, a clock correlates its internal clock ticks with the system time. (The system time is the time returned by the high-resolution performance counter.) This method returns:

<ul>
<li>
            The most recent clock time that was correlated with system time.
          </li>
<li>
            The system time when the correlation was performed.
          </li>
</ul>

        The clock time is returned in the <i>pllClockTime</i> parameter and is expressed in units of the clock's frequency. If the clock's <a href="https://msdn.microsoft.com/50a81e8b-9aa8-484c-afb7-950068feefc4">IMFClock::GetClockCharacteristics</a> method returns the <b>MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ</b> flag, the clock's frequency is 10 MHz (each clock tick is 100 nanoseconds). Otherwise, you can get the clock's frequency by calling <a href="https://msdn.microsoft.com/9dfc0efc-d274-45a6-b1ab-30f6215fbed8">IMFClock::GetProperties</a>. The frequency is given in the <b>qwClockFrequency</b> member of the <a href="https://msdn.microsoft.com/1efc6602-9851-40e5-85aa-0335d4e899a2">MFCLOCK_PROPERTIES</a> structure returned by that method.
      


        The system time is returned in the <i>phnsSystemTime</i> parameter, and is always expressed in 100-nanosecond units.
      


        To find out how often the clock correlates its clock time with the system time, call <a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>. The correlation interval is given in the <b>qwCorrelationRate</b> member of the <a href="https://msdn.microsoft.com/1efc6602-9851-40e5-85aa-0335d4e899a2">MFCLOCK_PROPERTIES</a> structure. If <b>qwCorrelationRate</b> is zero, it means the clock performs the correlation whenever <b>GetCorrelatedTime</b> is called. Otherwise, you can calculate the current clock time by extrapolating from the last correlated time.
      


        Some clocks support rate changes through the <a href="https://msdn.microsoft.com/54303c32-b260-4364-9130-a592694f2816">IMFRateControl</a> interface. If so, the clock time advances at a speed of frequency × current rate. If a clock does not expose the <b>IMFRateControl</b> interface, the rate is always 1.0.
      

For the presentation clock, the clock time is the presentation time, and is always relative to the starting time specified in <a href="https://msdn.microsoft.com/ba5986d1-9c94-4747-a221-43d0583f1fed">IMFPresentationClock::Start</a>. You can also get the presentation time by calling <a href="https://msdn.microsoft.com/31037b75-9fa5-48e0-a58c-a451b445147f">IMFPresentationClock::GetTime</a>.




## -see-also




<a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>
 

 

