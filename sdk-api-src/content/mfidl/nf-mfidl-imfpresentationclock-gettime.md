---
UID: NF:mfidl.IMFPresentationClock.GetTime
title: IMFPresentationClock::GetTime (mfidl.h)
description: Retrieves the latest clock time.
helpviewer_keywords: ["31037b75-9fa5-48e0-a58c-a451b445147f","GetTime","GetTime method [Media Foundation]","GetTime method [Media Foundation]","IMFPresentationClock interface","IMFPresentationClock interface [Media Foundation]","GetTime method","IMFPresentationClock.GetTime","IMFPresentationClock::GetTime","mf.imfpresentationclock_gettime","mfidl/IMFPresentationClock::GetTime"]
old-location: mf\imfpresentationclock_gettime.htm
tech.root: mf
ms.assetid: 31037b75-9fa5-48e0-a58c-a451b445147f
ms.date: 12/05/2018
ms.keywords: 31037b75-9fa5-48e0-a58c-a451b445147f, GetTime, GetTime method [Media Foundation], GetTime method [Media Foundation],IMFPresentationClock interface, IMFPresentationClock interface [Media Foundation],GetTime method, IMFPresentationClock.GetTime, IMFPresentationClock::GetTime, mf.imfpresentationclock_gettime, mfidl/IMFPresentationClock::GetTime
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPresentationClock::GetTime
 - mfidl/IMFPresentationClock::GetTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPresentationClock.GetTime
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
The clock does not have a presentation time source. Call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource">IMFPresentationClock::SetTimeSource</a>.
              

</td>
</tr>
</table>

## -remarks

This method does not attempt to smooth out jitter or otherwise account for any inaccuracies in the clock time.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>