---
UID: NF:mfidl.IMFClock.GetProperties
title: IMFClock::GetProperties
author: windows-sdk-content
description: Retrieves the properties of the clock.
old-location: mf\imfclock_getproperties.htm
tech.root: medfound
ms.assetid: 9dfc0efc-d274-45a6-b1ab-30f6215fbed8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 9dfc0efc-d274-45a6-b1ab-30f6215fbed8, GetProperties, GetProperties method [Media Foundation], GetProperties method [Media Foundation],IMFClock interface, IMFClock interface [Media Foundation],GetProperties method, IMFClock.GetProperties, IMFClock::GetProperties, mf.imfclock_getproperties, mfidl/IMFClock::GetProperties
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
 - IMFClock.GetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFClock::GetProperties


## -description



Retrieves the properties of the clock.




## -parameters




### -param pClockProperties [out]

Pointer to an <a href="https://msdn.microsoft.com/1efc6602-9851-40e5-85aa-0335d4e899a2">MFCLOCK_PROPERTIES</a> structure that receives the properties.


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
 




## -see-also




<a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a>
 

 

