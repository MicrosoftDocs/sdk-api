---
UID: NF:mfidl.IMFPresentationClock.SetTimeSource
title: IMFPresentationClock::SetTimeSource (mfidl.h)
description: Sets the time source for the presentation clock. The time source is the object that drives the clock by providing the current time.
helpviewer_keywords: ["170b7c8e-9d1a-4168-964a-5fd057d1e8f9","IMFPresentationClock interface [Media Foundation]","SetTimeSource method","IMFPresentationClock.SetTimeSource","IMFPresentationClock::SetTimeSource","SetTimeSource","SetTimeSource method [Media Foundation]","SetTimeSource method [Media Foundation]","IMFPresentationClock interface","mf.imfpresentationclock_settimesource","mfidl/IMFPresentationClock::SetTimeSource"]
old-location: mf\imfpresentationclock_settimesource.htm
tech.root: mf
ms.assetid: 170b7c8e-9d1a-4168-964a-5fd057d1e8f9
ms.date: 12/05/2018
ms.keywords: 170b7c8e-9d1a-4168-964a-5fd057d1e8f9, IMFPresentationClock interface [Media Foundation],SetTimeSource method, IMFPresentationClock.SetTimeSource, IMFPresentationClock::SetTimeSource, SetTimeSource, SetTimeSource method [Media Foundation], SetTimeSource method [Media Foundation],IMFPresentationClock interface, mf.imfpresentationclock_settimesource, mfidl/IMFPresentationClock::SetTimeSource
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
 - IMFPresentationClock::SetTimeSource
 - mfidl/IMFPresentationClock::SetTimeSource
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
 - IMFPresentationClock.SetTimeSource
---

# IMFPresentationClock::SetTimeSource


## -description

Sets the time source for the presentation clock. The time source is the object that drives the clock by providing the current time.

## -parameters

### -param pTimeSource [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource">IMFPresentationTimeSource</a> interface of the time source.

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
<dt><b>MF_E_CLOCK_NOT_SIMPLE</b></dt>
</dl>
</td>
<td width="60%">
The time source does not have a frequency of 10 MHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The time source has not been initialized.

</td>
</tr>
</table>

## -remarks

The presentation clock cannot start until it has a time source.

The time source is automatically registered to receive state change notifications from the clock, through the time source's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a> interface, which all time sources must implement.

This time source have a frequency of 10 MHz. See <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclock-getclockcharacteristics">IMFClock::GetClockCharacteristics</a>. If not, the method returns MF_E_CLOCK_NOT_SIMPLE.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>