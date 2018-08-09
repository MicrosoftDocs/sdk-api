---
UID: NF:wmsdkidl.IWMReaderStreamClock.SetTimer
title: IWMReaderStreamClock::SetTimer
author: windows-sdk-content
description: The SetTimer method sets a timer on the clock.
old-location: wmformat\iwmreaderstreamclock_settimer.htm
old-project: wmformat
ms.assetid: 15d991e0-a271-4427-844f-5e4a9bbc6507
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderStreamClock interface [windows Media Format],SetTimer method, IWMReaderStreamClock.SetTimer, IWMReaderStreamClock::SetTimer, IWMReaderStreamClockSetTimer, SetTimer, SetTimer method [windows Media Format], SetTimer method [windows Media Format],IWMReaderStreamClock interface, wmformat.iwmreaderstreamclock_settimer, wmsdkidl/IWMReaderStreamClock::SetTimer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderStreamClock::SetTimer


## -description



The <b>SetTimer</b> method sets a timer on the clock.




## -parameters




### -param cnsWhen [in]

Specifies the time at which the reader notifies the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">OnStatus</a> callback, in 100-nanosecond units.


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



The application must execute <a href="https://msdn.microsoft.com/ab5b7f9e-b647-4121-abb3-2c9deb1f50cc">IWMReader::Open</a>, and successfully receive a WMT_OPENED status notification to its <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> method, before it creates any timers.

All timers are automatically terminated when the application stops the reader. When a timer expires, the following happens: 

<ul>
<li>The <b>OnStatus</b> method is called with WMT_TIMER, as the <a href="https://msdn.microsoft.com/ebf77e8a-65e8-4da9-bb21-a1e2bf427bbf">WMT_STATUS</a> enumeration type</li>
<li>The parameter <i>hr</i> is set to S_OK</li>
<li><i>pValue</i> is set to the TimerID</li>
<li><i>pvContext</i> is set to the <i>pvParam</i> pointer that is specified in this method</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/0f170b6d-fd93-4bf8-8a98-f2a80f03b380">IWMReaderStreamClock Interface</a>



<a href="https://msdn.microsoft.com/d44b8701-8065-40a5-abc3-1c7513c618ea">IWMReaderStreamClock::GetTime</a>
 

 

