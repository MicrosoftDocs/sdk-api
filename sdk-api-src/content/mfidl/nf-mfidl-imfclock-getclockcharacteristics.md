---
UID: NF:mfidl.IMFClock.GetClockCharacteristics
title: IMFClock::GetClockCharacteristics (mfidl.h)
description: Retrieves the characteristics of the clock.
old-location: mf\imfclock_getclockcharacteristics.htm
tech.root: medfound
ms.assetid: 50a81e8b-9aa8-484c-afb7-950068feefc4
ms.date: 12/05/2018
ms.keywords: 50a81e8b-9aa8-484c-afb7-950068feefc4, GetClockCharacteristics, GetClockCharacteristics method [Media Foundation], GetClockCharacteristics method [Media Foundation],IMFClock interface, IMFClock interface [Media Foundation],GetClockCharacteristics method, IMFClock.GetClockCharacteristics, IMFClock::GetClockCharacteristics, mf.imfclock_getclockcharacteristics, mfidl/IMFClock::GetClockCharacteristics
ms.topic: method
f1_keywords:
- mfidl/IMFClock.GetClockCharacteristics
dev_langs:
- c++
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
- IMFClock.GetClockCharacteristics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFClock::GetClockCharacteristics


## -description



Retrieves the characteristics of the clock.




## -parameters




### -param pdwCharacteristics [out]

Receives a bitwise OR of values from the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ne-mfidl-mfclock_characteristics_flags">MFCLOCK_CHARACTERISTICS_FLAGS</a> enumeration indicating the characteristics of the clock.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>
 

 

