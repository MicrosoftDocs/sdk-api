---
UID: NF:mfidl.IMFPresentationClock.GetTimeSource
title: IMFPresentationClock::GetTimeSource (mfidl.h)
description: Retrieves the clock's presentation time source.
helpviewer_keywords: ["GetTimeSource","GetTimeSource method [Media Foundation]","GetTimeSource method [Media Foundation]","IMFPresentationClock interface","IMFPresentationClock interface [Media Foundation]","GetTimeSource method","IMFPresentationClock.GetTimeSource","IMFPresentationClock::GetTimeSource","e6b6851b-f5b3-40c2-9160-59f2a68c9131","mf.imfpresentationclock_gettimesource","mfidl/IMFPresentationClock::GetTimeSource"]
old-location: mf\imfpresentationclock_gettimesource.htm
tech.root: mf
ms.assetid: e6b6851b-f5b3-40c2-9160-59f2a68c9131
ms.date: 12/05/2018
ms.keywords: GetTimeSource, GetTimeSource method [Media Foundation], GetTimeSource method [Media Foundation],IMFPresentationClock interface, IMFPresentationClock interface [Media Foundation],GetTimeSource method, IMFPresentationClock.GetTimeSource, IMFPresentationClock::GetTimeSource, e6b6851b-f5b3-40c2-9160-59f2a68c9131, mf.imfpresentationclock_gettimesource, mfidl/IMFPresentationClock::GetTimeSource
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
 - IMFPresentationClock::GetTimeSource
 - mfidl/IMFPresentationClock::GetTimeSource
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
 - IMFPresentationClock.GetTimeSource
---

# IMFPresentationClock::GetTimeSource


## -description

Retrieves the clock's presentation time source.

## -parameters

### -param ppTimeSource [out]

Receives a pointer to the time source's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource">IMFPresentationTimeSource</a> interface. The caller must release the interface.

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
No time source was set on this clock.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>