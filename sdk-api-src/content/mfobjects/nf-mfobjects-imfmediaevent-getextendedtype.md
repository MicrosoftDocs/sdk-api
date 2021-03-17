---
UID: NF:mfobjects.IMFMediaEvent.GetExtendedType
title: IMFMediaEvent::GetExtendedType (mfobjects.h)
description: Retrieves the extended type of the event.
helpviewer_keywords: ["56284491-6f84-467e-9fac-46b04db4024a","GetExtendedType","GetExtendedType method [Media Foundation]","GetExtendedType method [Media Foundation]","IMFMediaEvent interface","IMFMediaEvent interface [Media Foundation]","GetExtendedType method","IMFMediaEvent.GetExtendedType","IMFMediaEvent::GetExtendedType","mf.imfmediaevent_getextendedtype","mfobjects/IMFMediaEvent::GetExtendedType"]
old-location: mf\imfmediaevent_getextendedtype.htm
tech.root: mf
ms.assetid: 56284491-6f84-467e-9fac-46b04db4024a
ms.date: 12/05/2018
ms.keywords: 56284491-6f84-467e-9fac-46b04db4024a, GetExtendedType, GetExtendedType method [Media Foundation], GetExtendedType method [Media Foundation],IMFMediaEvent interface, IMFMediaEvent interface [Media Foundation],GetExtendedType method, IMFMediaEvent.GetExtendedType, IMFMediaEvent::GetExtendedType, mf.imfmediaevent_getextendedtype, mfobjects/IMFMediaEvent::GetExtendedType
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFMediaEvent::GetExtendedType
 - mfobjects/IMFMediaEvent::GetExtendedType
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
 - IMFMediaEvent.GetExtendedType
---

# IMFMediaEvent::GetExtendedType


## -description

Retrieves the extended type of the event.

## -parameters

### -param pguidExtendedType [out]

Receives a <b>GUID</b> that identifies the extended type.

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

To define a custom event, create a new extended-type GUID and send an <a href="/windows/desktop/medfound/meextendedtype">MEExtendedType</a> event with that GUID.

Some standard Media Foundation events also use the extended type to differentiate between types of event data.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a>



<a href="/windows/desktop/medfound/media-event-generators">Media Event Generators</a>