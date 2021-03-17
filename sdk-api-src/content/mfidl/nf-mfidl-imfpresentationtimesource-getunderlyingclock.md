---
UID: NF:mfidl.IMFPresentationTimeSource.GetUnderlyingClock
title: IMFPresentationTimeSource::GetUnderlyingClock (mfidl.h)
description: Retrieves the underlying clock that the presentation time source uses to generate its clock times.
helpviewer_keywords: ["09c8fef8-7288-4356-9671-4c927c0cf502","GetUnderlyingClock","GetUnderlyingClock method [Media Foundation]","GetUnderlyingClock method [Media Foundation]","IMFPresentationTimeSource interface","IMFPresentationTimeSource interface [Media Foundation]","GetUnderlyingClock method","IMFPresentationTimeSource.GetUnderlyingClock","IMFPresentationTimeSource::GetUnderlyingClock","mf.imfpresentationtimesource_getunderlyingclock","mfidl/IMFPresentationTimeSource::GetUnderlyingClock"]
old-location: mf\imfpresentationtimesource_getunderlyingclock.htm
tech.root: mf
ms.assetid: 09c8fef8-7288-4356-9671-4c927c0cf502
ms.date: 12/05/2018
ms.keywords: 09c8fef8-7288-4356-9671-4c927c0cf502, GetUnderlyingClock, GetUnderlyingClock method [Media Foundation], GetUnderlyingClock method [Media Foundation],IMFPresentationTimeSource interface, IMFPresentationTimeSource interface [Media Foundation],GetUnderlyingClock method, IMFPresentationTimeSource.GetUnderlyingClock, IMFPresentationTimeSource::GetUnderlyingClock, mf.imfpresentationtimesource_getunderlyingclock, mfidl/IMFPresentationTimeSource::GetUnderlyingClock
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
 - IMFPresentationTimeSource::GetUnderlyingClock
 - mfidl/IMFPresentationTimeSource::GetUnderlyingClock
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
 - IMFPresentationTimeSource.GetUnderlyingClock
---

# IMFPresentationTimeSource::GetUnderlyingClock


## -description

Retrieves the underlying clock that the presentation time source uses to generate its clock times.

## -parameters

### -param ppClock [out]

Receives a pointer to the clock's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a> interface. The caller must release the interface.

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
<dt><b>MF_E_NO_CLOCK</b></dt>
</dl>
</td>
<td width="60%">
This time source does not expose an underlying clock.

</td>
</tr>
</table>

## -remarks

A presentation time source must support stopping, starting, pausing, and rate changes. However, in many cases the time source derives its clock times from a hardware clock or other device. The underlying clock is always running, and might not support rate changes.

Optionally, a time source can expose the underlying clock by implementing this method. The underlying clock is always running, even when the presentation time source is paused or stopped. (Therefore, the underlying clock returns the MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING flag in the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclock-getclockcharacteristics">IMFClock::GetClockCharacteristics</a> method).

The underlying clock is useful if you want to make decisions based on the clock times while the presentation clock is stopped or paused.

If the time source does not expose an underlying clock, the method returns MF_E_NO_CLOCK.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource">IMFPresentationTimeSource</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>