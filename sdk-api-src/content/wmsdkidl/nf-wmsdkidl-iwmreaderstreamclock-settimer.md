---
UID: NF:wmsdkidl.IWMReaderStreamClock.SetTimer
title: IWMReaderStreamClock::SetTimer (wmsdkidl.h)
description: The SetTimer method sets a timer on the clock.
helpviewer_keywords: ["IWMReaderStreamClock interface [windows Media Format]","SetTimer method","IWMReaderStreamClock.SetTimer","IWMReaderStreamClock::SetTimer","IWMReaderStreamClockSetTimer","SetTimer","SetTimer method [windows Media Format]","SetTimer method [windows Media Format]","IWMReaderStreamClock interface","wmformat.iwmreaderstreamclock_settimer","wmsdkidl/IWMReaderStreamClock::SetTimer"]
old-location: wmformat\iwmreaderstreamclock_settimer.htm
tech.root: wmformat
ms.assetid: 15d991e0-a271-4427-844f-5e4a9bbc6507
ms.date: 4/26/2023
ms.keywords: IWMReaderStreamClock interface [windows Media Format],SetTimer method, IWMReaderStreamClock.SetTimer, IWMReaderStreamClock::SetTimer, IWMReaderStreamClockSetTimer, SetTimer, SetTimer method [windows Media Format], SetTimer method [windows Media Format],IWMReaderStreamClock interface, wmformat.iwmreaderstreamclock_settimer, wmsdkidl/IWMReaderStreamClock::SetTimer
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
 - IWMReaderStreamClock::SetTimer
 - wmsdkidl/IWMReaderStreamClock::SetTimer
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
 - IWMReaderStreamClock.SetTimer
---

# IWMReaderStreamClock::SetTimer


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetTimer</b> method sets a timer on the clock.

## -parameters

### -param cnsWhen [in]

Specifies the time at which the reader notifies the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">OnStatus</a> callback, in 100-nanosecond units.

### -param pvParam [in]

Specifies a pointer to the timer context parameters that are returned in the <b>OnStatus</b> callback.

### -param pdwTimerId [out]

Pointer to a <b>DWORD</b> containing the timer identifier.

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
<i>pdwTimerId</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough available memory.

</td>
</tr>
</table>

## -remarks

The application must execute <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>, and successfully receive a WMT_OPENED status notification to its <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method, before it creates any timers.

All timers are automatically terminated when the application stops the reader. When a timer expires, the following happens: 

<ul>
<li>The <b>OnStatus</b> method is called with WMT_TIMER, as the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status">WMT_STATUS</a> enumeration type</li>
<li>The parameter <i>hr</i> is set to S_OK</li>
<li><i>pValue</i> is set to the TimerID</li>
<li><i>pvContext</i> is set to the <i>pvParam</i> pointer that is specified in this method</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock">IWMReaderStreamClock Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderstreamclock-gettime">IWMReaderStreamClock::GetTime</a>