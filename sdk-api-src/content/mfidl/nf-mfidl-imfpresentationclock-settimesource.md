---
UID: NF:mfidl.IMFPresentationClock.SetTimeSource
title: IMFPresentationClock::SetTimeSource
author: windows-sdk-content
description: Sets the time source for the presentation clock. The time source is the object that drives the clock by providing the current time.
old-location: mf\imfpresentationclock_settimesource.htm
tech.root: medfound
ms.assetid: 170b7c8e-9d1a-4168-964a-5fd057d1e8f9
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 170b7c8e-9d1a-4168-964a-5fd057d1e8f9, IMFPresentationClock interface [Media Foundation],SetTimeSource method, IMFPresentationClock.SetTimeSource, IMFPresentationClock::SetTimeSource, SetTimeSource, SetTimeSource method [Media Foundation], SetTimeSource method [Media Foundation],IMFPresentationClock interface, mf.imfpresentationclock_settimesource, mfidl/IMFPresentationClock::SetTimeSource
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
 - IMFPresentationClock.SetTimeSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationClock::SetTimeSource


## -description



Sets the time source for the presentation clock. The time source is the object that drives the clock by providing the current time.




## -parameters




### -param pTimeSource [in]

Pointer to the <a href="https://msdn.microsoft.com/e5fab6b7-0abc-4ad7-89a9-33c673e97ce2">IMFPresentationTimeSource</a> interface of the time source.


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
<dt><b>MF_E_CLOCK_NOT_SIMPLE</b></dt>
</dl>
</td>
<td width="60%">
The time source does not have a frequency of 10 MHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The time source has not been initialized.

</td>
</tr>
</table>
 




## -remarks



The presentation clock cannot start until it has a time source.

The time source is automatically registered to receive state change notifications from the clock, through the time source's <a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a> interface, which all time sources must implement.

This time source have a frequency of 10 MHz. See <a href="https://msdn.microsoft.com/50a81e8b-9aa8-484c-afb7-950068feefc4">IMFClock::GetClockCharacteristics</a>. If not, the method returns MF_E_CLOCK_NOT_SIMPLE.




## -see-also




<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

