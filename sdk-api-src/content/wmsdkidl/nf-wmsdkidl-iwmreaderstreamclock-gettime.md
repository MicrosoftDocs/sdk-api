---
UID: NF:wmsdkidl.IWMReaderStreamClock.GetTime
title: IWMReaderStreamClock::GetTime (wmsdkidl.h)
description: The GetTime method retrieves the current value of the stream clock.
helpviewer_keywords: ["GetTime","GetTime method [windows Media Format]","GetTime method [windows Media Format]","IWMReaderStreamClock interface","IWMReaderStreamClock interface [windows Media Format]","GetTime method","IWMReaderStreamClock.GetTime","IWMReaderStreamClock::GetTime","IWMReaderStreamClockGetTime","wmformat.iwmreaderstreamclock_gettime","wmsdkidl/IWMReaderStreamClock::GetTime"]
old-location: wmformat\iwmreaderstreamclock_gettime.htm
tech.root: wmformat
ms.assetid: d44b8701-8065-40a5-abc3-1c7513c618ea
ms.date: 12/05/2018
ms.keywords: GetTime, GetTime method [windows Media Format], GetTime method [windows Media Format],IWMReaderStreamClock interface, IWMReaderStreamClock interface [windows Media Format],GetTime method, IWMReaderStreamClock.GetTime, IWMReaderStreamClock::GetTime, IWMReaderStreamClockGetTime, wmformat.iwmreaderstreamclock_gettime, wmsdkidl/IWMReaderStreamClock::GetTime
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderStreamClock::GetTime
 - wmsdkidl/IWMReaderStreamClock::GetTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderStreamClock.GetTime
---

# IWMReaderStreamClock::GetTime


## -description

The <b>GetTime</b> method retrieves the current value of the stream clock.

## -parameters

### -param pcnsNow [out]

Pointer to the current time of the stream clock, in 100-nanosecond units.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pcnsNow</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock">IWMReaderStreamClock Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderstreamclock-settimer">IWMReaderStreamClock::SetTimer</a>