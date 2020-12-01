---
UID: NF:mfidl.IMFClock.GetProperties
title: IMFClock::GetProperties (mfidl.h)
description: Retrieves the properties of the clock.
helpviewer_keywords: ["9dfc0efc-d274-45a6-b1ab-30f6215fbed8","GetProperties","GetProperties method [Media Foundation]","GetProperties method [Media Foundation]","IMFClock interface","IMFClock interface [Media Foundation]","GetProperties method","IMFClock.GetProperties","IMFClock::GetProperties","mf.imfclock_getproperties","mfidl/IMFClock::GetProperties"]
old-location: mf\imfclock_getproperties.htm
tech.root: mf
ms.assetid: 9dfc0efc-d274-45a6-b1ab-30f6215fbed8
ms.date: 12/05/2018
ms.keywords: 9dfc0efc-d274-45a6-b1ab-30f6215fbed8, GetProperties, GetProperties method [Media Foundation], GetProperties method [Media Foundation],IMFClock interface, IMFClock interface [Media Foundation],GetProperties method, IMFClock.GetProperties, IMFClock::GetProperties, mf.imfclock_getproperties, mfidl/IMFClock::GetProperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFClock::GetProperties
 - mfidl/IMFClock::GetProperties
dev_langs:
 - c++
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
---

# IMFClock::GetProperties


## -description

Retrieves the properties of the clock.

## -parameters

### -param pClockProperties [out]

Pointer to an <a href="/windows/desktop/api/mfidl/ns-mfidl-mfclock_properties">MFCLOCK_PROPERTIES</a> structure that receives the properties.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>