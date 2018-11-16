---
UID: NN:mfidl.IMFClock
title: IMFClock
author: windows-sdk-content
description: Provides timing information from a clock in Microsoft Media Foundation.
old-location: mf\imfclock.htm
tech.root: medfound
ms.assetid: 3a60bfec-8511-4a84-a833-e0c73c593970
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 3a60bfec-8511-4a84-a833-e0c73c593970, IMFClock, IMFClock interface [Media Foundation], IMFClock interface [Media Foundation],described, mf.imfclock, mfidl/IMFClock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFClock interface


## -description


Provides timing information from a clock in Microsoft Media Foundation.

Clocks and some media sinks expose this interface through <b>QueryInterface</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFClock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFClock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFClock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50a81e8b-9aa8-484c-afb7-950068feefc4">GetClockCharacteristics</a>
</td>
<td align="left" width="63%">
Retrieves the characteristics of the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8afda8c7-bab6-40fd-b20c-6bb29ed4900f">GetContinuityKey</a>
</td>
<td align="left" width="63%">
Retrieves the clock's continuity key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a897426-d994-4b27-9f13-9b0c7c9b3a9b">GetCorrelatedTime</a>
</td>
<td align="left" width="63%">
Retrieves the last clock time that was correlated with system time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dfc0efc-d274-45a6-b1ab-30f6215fbed8">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e2dda03-f589-4572-b715-2be7b29a6ace">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the clock.

</td>
</tr>
</table> 


## -remarks



The <b>IMFClock</b> interface applies to any kind of clock. The presentation clock exposes the <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a> interface in addition to <b>IMFClock</b>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

