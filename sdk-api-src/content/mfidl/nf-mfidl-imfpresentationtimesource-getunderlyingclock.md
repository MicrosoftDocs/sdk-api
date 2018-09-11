---
UID: NF:mfidl.IMFPresentationTimeSource.GetUnderlyingClock
title: IMFPresentationTimeSource::GetUnderlyingClock
author: windows-sdk-content
description: Retrieves the underlying clock that the presentation time source uses to generate its clock times.
old-location: mf\imfpresentationtimesource_getunderlyingclock.htm
tech.root: medfound
ms.assetid: 09c8fef8-7288-4356-9671-4c927c0cf502
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 09c8fef8-7288-4356-9671-4c927c0cf502, GetUnderlyingClock, GetUnderlyingClock method [Media Foundation], GetUnderlyingClock method [Media Foundation],IMFPresentationTimeSource interface, IMFPresentationTimeSource interface [Media Foundation],GetUnderlyingClock method, IMFPresentationTimeSource.GetUnderlyingClock, IMFPresentationTimeSource::GetUnderlyingClock, mf.imfpresentationtimesource_getunderlyingclock, mfidl/IMFPresentationTimeSource::GetUnderlyingClock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFPresentationTimeSource.GetUnderlyingClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationTimeSource::GetUnderlyingClock


## -description



Retrieves the underlying clock that the presentation time source uses to generate its clock times.




## -parameters




### -param ppClock [out]

Receives a pointer to the clock's <a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a> interface. The caller must release the interface.


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
<dt><b>MF_E_NO_CLOCK</b></dt>
</dl>
</td>
<td width="60%">
This time source does not expose an underlying clock.

</td>
</tr>
</table>
 




## -remarks



A presentation time source must support stopping, starting, pausing, and rate changes. However, in many cases the time source derives its clock times from a hardware clock or other device. The underlying clock is always running, and might not support rate changes.

Optionally, a time source can expose the underlying clock by implementing this method. The underlying clock is always running, even when the presentation time source is paused or stopped. (Therefore, the underlying clock returns the MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING flag in the <a href="https://msdn.microsoft.com/50a81e8b-9aa8-484c-afb7-950068feefc4">IMFClock::GetClockCharacteristics</a> method).

The underlying clock is useful if you want to make decisions based on the clock times while the presentation clock is stopped or paused.

If the time source does not expose an underlying clock, the method returns MF_E_NO_CLOCK.




## -see-also




<a href="https://msdn.microsoft.com/e5fab6b7-0abc-4ad7-89a9-33c673e97ce2">IMFPresentationTimeSource</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

