---
UID: NF:wmsdkidl.IWMReaderStreamClock.GetTime
title: IWMReaderStreamClock::GetTime method
author: windows-driver-content
description: The GetTime method retrieves the current value of the stream clock.
old-location: wmformat\iwmreaderstreamclock_gettime.htm
old-project: wmformat
ms.assetid: d44b8701-8065-40a5-abc3-1c7513c618ea
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetTime method [windows Media Format], GetTime method [windows Media Format], IWMReaderStreamClock interface, GetTime,IWMReaderStreamClock.GetTime, IWMReaderStreamClock, IWMReaderStreamClock interface [windows Media Format], GetTime method, IWMReaderStreamClock::GetTime, IWMReaderStreamClockGetTime, wmformat.iwmreaderstreamclock_gettime, wmsdkidl/IWMReaderStreamClock::GetTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderStreamClock.GetTime
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderStreamClock::GetTime method


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




<a href="https://msdn.microsoft.com/0f170b6d-fd93-4bf8-8a98-f2a80f03b380">IWMReaderStreamClock Interface</a>



<a href="https://msdn.microsoft.com/15d991e0-a271-4427-844f-5e4a9bbc6507">IWMReaderStreamClock::SetTimer</a>
 

 

