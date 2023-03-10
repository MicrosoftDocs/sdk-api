---
UID: NF:mfidl.IMFClock.GetContinuityKey
title: IMFClock::GetContinuityKey (mfidl.h)
description: Retrieves the clock's continuity key. (Not supported.).
helpviewer_keywords: ["8afda8c7-bab6-40fd-b20c-6bb29ed4900f","GetContinuityKey","GetContinuityKey method [Media Foundation]","GetContinuityKey method [Media Foundation]","IMFClock interface","IMFClock interface [Media Foundation]","GetContinuityKey method","IMFClock.GetContinuityKey","IMFClock::GetContinuityKey","mf.imfclock_getcontinuitykey","mfidl/IMFClock::GetContinuityKey"]
old-location: mf\imfclock_getcontinuitykey.htm
tech.root: mf
ms.assetid: 8afda8c7-bab6-40fd-b20c-6bb29ed4900f
ms.date: 12/05/2018
ms.keywords: 8afda8c7-bab6-40fd-b20c-6bb29ed4900f, GetContinuityKey, GetContinuityKey method [Media Foundation], GetContinuityKey method [Media Foundation],IMFClock interface, IMFClock interface [Media Foundation],GetContinuityKey method, IMFClock.GetContinuityKey, IMFClock::GetContinuityKey, mf.imfclock_getcontinuitykey, mfidl/IMFClock::GetContinuityKey
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
 - IMFClock::GetContinuityKey
 - mfidl/IMFClock::GetContinuityKey
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
 - IMFClock.GetContinuityKey
---

# IMFClock::GetContinuityKey


## -description

Retrieves the clock's continuity key. (Not supported.)

## -parameters

### -param pdwContinuityKey [out]

Receives the continuity key.

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
</table>

## -remarks

Continuity keys are currently not supported in Media Foundation. Clocks must return the value zero in the <i>pdwContinuityKey</i> parameter.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>