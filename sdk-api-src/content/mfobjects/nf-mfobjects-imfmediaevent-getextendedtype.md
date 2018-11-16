---
UID: NF:mfobjects.IMFMediaEvent.GetExtendedType
title: IMFMediaEvent::GetExtendedType
author: windows-sdk-content
description: Retrieves the extended type of the event.
old-location: mf\imfmediaevent_getextendedtype.htm
tech.root: medfound
ms.assetid: 56284491-6f84-467e-9fac-46b04db4024a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 56284491-6f84-467e-9fac-46b04db4024a, GetExtendedType, GetExtendedType method [Media Foundation], GetExtendedType method [Media Foundation],IMFMediaEvent interface, IMFMediaEvent interface [Media Foundation],GetExtendedType method, IMFMediaEvent.GetExtendedType, IMFMediaEvent::GetExtendedType, mf.imfmediaevent_getextendedtype, mfobjects/IMFMediaEvent::GetExtendedType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfobjects.h
: 
- IMFMediaEvent.GetExtendedType
: 
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



To define a custom event, create a new extended-type GUID and send an <a href="https://msdn.microsoft.com/a54a446c-0e96-467b-90f6-0f64a7c1727d">MEExtendedType</a> event with that GUID.

Some standard Media Foundation events also use the extended type to differentiate between types of event data.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a>



<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>
 

 

