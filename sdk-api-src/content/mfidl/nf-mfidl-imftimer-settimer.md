---
UID: NF:mfidl.IMFTimer.SetTimer
title: IMFTimer::SetTimer (mfidl.h)
description: Sets a timer that invokes a callback at the specified time.
helpviewer_keywords: ["3b583541-6480-490d-883f-376ea95f7a98","IMFTimer interface [Media Foundation]","SetTimer method","IMFTimer.SetTimer","IMFTimer::SetTimer","SetTimer","SetTimer method [Media Foundation]","SetTimer method [Media Foundation]","IMFTimer interface","mf.imftimer_settimer","mfidl/IMFTimer::SetTimer"]
old-location: mf\imftimer_settimer.htm
tech.root: mf
ms.assetid: 3b583541-6480-490d-883f-376ea95f7a98
ms.date: 12/05/2018
ms.keywords: 3b583541-6480-490d-883f-376ea95f7a98, IMFTimer interface [Media Foundation],SetTimer method, IMFTimer.SetTimer, IMFTimer::SetTimer, SetTimer, SetTimer method [Media Foundation], SetTimer method [Media Foundation],IMFTimer interface, mf.imftimer_settimer, mfidl/IMFTimer::SetTimer
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFTimer::SetTimer
 - mfidl/IMFTimer::SetTimer
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
 - IMFTimer.SetTimer
---

# IMFTimer::SetTimer


## -description

Sets a timer that invokes a callback at the specified time.

## -parameters

### -param dwFlags [in]

Bitwise OR of zero or more flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mftimer_flags">MFTIMER_FLAGS</a> enumeration.

### -param llClockTime [in]

The time at which the timer should fire, in units of the clock's frequency. The time is either absolute or relative to the current time, depending on the value of <i>dwFlags</i>.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface. The callback's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">Invoke</a> method is called at the time specified in the <i>llClockTime</i> parameter.

### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

### -param ppunkKey [out]

Receives a pointer to the <b>IUnknown</b> interface of a cancellation object. The caller must release the interface. To cancel the timer, pass this pointer to the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftimer-canceltimer">IMFTimer::CancelTimer</a> method. This parameter can be <b>NULL</b>.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The clock was shut down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_CLOCK_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, but the clock is stopped.

</td>
</tr>
</table>

## -remarks

If the clock is stopped, the method returns MF_S_CLOCK_STOPPED. The callback will not be invoked until the clock is started.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftimer">IMFTimer</a>