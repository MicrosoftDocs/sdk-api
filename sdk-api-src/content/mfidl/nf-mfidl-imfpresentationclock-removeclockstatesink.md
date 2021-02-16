---
UID: NF:mfidl.IMFPresentationClock.RemoveClockStateSink
title: IMFPresentationClock::RemoveClockStateSink (mfidl.h)
description: Unregisters an object that is receiving state-change notifications from the clock.
helpviewer_keywords: ["IMFPresentationClock interface [Media Foundation]","RemoveClockStateSink method","IMFPresentationClock.RemoveClockStateSink","IMFPresentationClock::RemoveClockStateSink","RemoveClockStateSink","RemoveClockStateSink method [Media Foundation]","RemoveClockStateSink method [Media Foundation]","IMFPresentationClock interface","c037183d-a81f-4f49-9e02-06dc2476471f","mf.imfpresentationclock_removeclockstatesink","mfidl/IMFPresentationClock::RemoveClockStateSink"]
old-location: mf\imfpresentationclock_removeclockstatesink.htm
tech.root: mf
ms.assetid: c037183d-a81f-4f49-9e02-06dc2476471f
ms.date: 12/05/2018
ms.keywords: IMFPresentationClock interface [Media Foundation],RemoveClockStateSink method, IMFPresentationClock.RemoveClockStateSink, IMFPresentationClock::RemoveClockStateSink, RemoveClockStateSink, RemoveClockStateSink method [Media Foundation], RemoveClockStateSink method [Media Foundation],IMFPresentationClock interface, c037183d-a81f-4f49-9e02-06dc2476471f, mf.imfpresentationclock_removeclockstatesink, mfidl/IMFPresentationClock::RemoveClockStateSink
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
 - IMFPresentationClock::RemoveClockStateSink
 - mfidl/IMFPresentationClock::RemoveClockStateSink
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
 - IMFPresentationClock.RemoveClockStateSink
---

# IMFPresentationClock::RemoveClockStateSink


## -description

Unregisters an object that is receiving state-change notifications from the clock.

## -parameters

### -param pStateSink [in]

Pointer to the object's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a> interface.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>