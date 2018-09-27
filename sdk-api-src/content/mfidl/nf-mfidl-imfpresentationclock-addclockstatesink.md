---
UID: NF:mfidl.IMFPresentationClock.AddClockStateSink
title: IMFPresentationClock::AddClockStateSink
author: windows-sdk-content
description: Registers an object to be notified whenever the clock starts, stops, or pauses, or changes rate.
old-location: mf\imfpresentationclock_addclockstatesink.htm
tech.root: medfound
ms.assetid: c90c3d26-51fa-4cd6-a154-6f72c21219d2
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: AddClockStateSink, AddClockStateSink method [Media Foundation], AddClockStateSink method [Media Foundation],IMFPresentationClock interface, IMFPresentationClock interface [Media Foundation],AddClockStateSink method, IMFPresentationClock.AddClockStateSink, IMFPresentationClock::AddClockStateSink, c90c3d26-51fa-4cd6-a154-6f72c21219d2, mf.imfpresentationclock_addclockstatesink, mfidl/IMFPresentationClock::AddClockStateSink
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
 - IMFPresentationClock.AddClockStateSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationClock::AddClockStateSink


## -description



Registers an object to be notified whenever the clock starts, stops, or pauses, or changes rate.




## -parameters




### -param pStateSink [in]

Pointer to the object's <a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a> interface.


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



Before releasing the object, call <a href="https://msdn.microsoft.com/c037183d-a81f-4f49-9e02-06dc2476471f">IMFPresentationClock::RemoveClockStateSink</a> to unregister the object for state-change notifications.




## -see-also




<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

