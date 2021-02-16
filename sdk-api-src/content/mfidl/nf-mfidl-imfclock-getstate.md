---
UID: NF:mfidl.IMFClock.GetState
title: IMFClock::GetState (mfidl.h)
description: Retrieves the current state of the clock.
helpviewer_keywords: ["8e2dda03-f589-4572-b715-2be7b29a6ace","GetState","GetState method [Media Foundation]","GetState method [Media Foundation]","IMFClock interface","IMFClock interface [Media Foundation]","GetState method","IMFClock.GetState","IMFClock::GetState","mf.imfclock_getstate","mfidl/IMFClock::GetState"]
old-location: mf\imfclock_getstate.htm
tech.root: mf
ms.assetid: 8e2dda03-f589-4572-b715-2be7b29a6ace
ms.date: 12/05/2018
ms.keywords: 8e2dda03-f589-4572-b715-2be7b29a6ace, GetState, GetState method [Media Foundation], GetState method [Media Foundation],IMFClock interface, IMFClock interface [Media Foundation],GetState method, IMFClock.GetState, IMFClock::GetState, mf.imfclock_getstate, mfidl/IMFClock::GetState
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
 - IMFClock::GetState
 - mfidl/IMFClock::GetState
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
 - IMFClock.GetState
---

# IMFClock::GetState


## -description

Retrieves the current state of the clock.

## -parameters

### -param dwReserved [in]

Reserved, must be zero.

### -param peClockState [out]

Receives the clock state, as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfclock_state">MFCLOCK_STATE</a> enumeration.

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

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>