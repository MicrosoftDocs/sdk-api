---
UID: NF:mfidl.IMFPresentationClock.AddClockStateSink
title: IMFPresentationClock::AddClockStateSink (mfidl.h)
description: Registers an object to be notified whenever the clock starts, stops, or pauses, or changes rate.
helpviewer_keywords: ["AddClockStateSink","AddClockStateSink method [Media Foundation]","AddClockStateSink method [Media Foundation]","IMFPresentationClock interface","IMFPresentationClock interface [Media Foundation]","AddClockStateSink method","IMFPresentationClock.AddClockStateSink","IMFPresentationClock::AddClockStateSink","c90c3d26-51fa-4cd6-a154-6f72c21219d2","mf.imfpresentationclock_addclockstatesink","mfidl/IMFPresentationClock::AddClockStateSink"]
old-location: mf\imfpresentationclock_addclockstatesink.htm
tech.root: mf
ms.assetid: c90c3d26-51fa-4cd6-a154-6f72c21219d2
ms.date: 12/05/2018
ms.keywords: AddClockStateSink, AddClockStateSink method [Media Foundation], AddClockStateSink method [Media Foundation],IMFPresentationClock interface, IMFPresentationClock interface [Media Foundation],AddClockStateSink method, IMFPresentationClock.AddClockStateSink, IMFPresentationClock::AddClockStateSink, c90c3d26-51fa-4cd6-a154-6f72c21219d2, mf.imfpresentationclock_addclockstatesink, mfidl/IMFPresentationClock::AddClockStateSink
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
 - IMFPresentationClock::AddClockStateSink
 - mfidl/IMFPresentationClock::AddClockStateSink
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
 - IMFPresentationClock.AddClockStateSink
---

# IMFPresentationClock::AddClockStateSink


## -description

Registers an object to be notified whenever the clock starts, stops, or pauses, or changes rate.

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

## -remarks

Before releasing the object, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink">IMFPresentationClock::RemoveClockStateSink</a> to unregister the object for state-change notifications.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>