---
UID: NF:mfidl.IMFPresentationClock.GetTimeSource
title: IMFPresentationClock::GetTimeSource
author: windows-sdk-content
description: Retrieves the clock's presentation time source.
old-location: mf\imfpresentationclock_gettimesource.htm
tech.root: medfound
ms.assetid: e6b6851b-f5b3-40c2-9160-59f2a68c9131
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetTimeSource, GetTimeSource method [Media Foundation], GetTimeSource method [Media Foundation],IMFPresentationClock interface, IMFPresentationClock interface [Media Foundation],GetTimeSource method, IMFPresentationClock.GetTimeSource, IMFPresentationClock::GetTimeSource, e6b6851b-f5b3-40c2-9160-59f2a68c9131, mf.imfpresentationclock_gettimesource, mfidl/IMFPresentationClock::GetTimeSource
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
 - IMFPresentationClock.GetTimeSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationClock::GetTimeSource


## -description



Retrieves the clock's presentation time source.




## -parameters




### -param ppTimeSource [out]

Receives a pointer to the time source's <a href="https://msdn.microsoft.com/e5fab6b7-0abc-4ad7-89a9-33c673e97ce2">IMFPresentationTimeSource</a> interface. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

