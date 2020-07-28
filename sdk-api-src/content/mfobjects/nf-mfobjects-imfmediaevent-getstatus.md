---
UID: NF:mfobjects.IMFMediaEvent.GetStatus
title: IMFMediaEvent::GetStatus (mfobjects.h)
description: Retrieves an HRESULT that specifies the event status.
helpviewer_keywords: ["GetStatus","GetStatus method [Media Foundation]","GetStatus method [Media Foundation]","IMFMediaEvent interface","IMFMediaEvent interface [Media Foundation]","GetStatus method","IMFMediaEvent.GetStatus","IMFMediaEvent::GetStatus","e2fc6c81-11c0-4947-b647-3e74a73ee5a2","mf.imfmediaevent_getstatus","mfobjects/IMFMediaEvent::GetStatus"]
old-location: mf\imfmediaevent_getstatus.htm
tech.root: mf
ms.assetid: e2fc6c81-11c0-4947-b647-3e74a73ee5a2
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Media Foundation], GetStatus method [Media Foundation],IMFMediaEvent interface, IMFMediaEvent interface [Media Foundation],GetStatus method, IMFMediaEvent.GetStatus, IMFMediaEvent::GetStatus, e2fc6c81-11c0-4947-b647-3e74a73ee5a2, mf.imfmediaevent_getstatus, mfobjects/IMFMediaEvent::GetStatus
f1_keywords:
- mfobjects/IMFMediaEvent.GetStatus
dev_langs:
- c++
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
- IMFMediaEvent.GetStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEvent::GetStatus


## -description



Retrieves an <b>HRESULT</b> that specifies the event status.




## -parameters




### -param phrStatus [out]

Receives the event status. If the operation that generated the event was successful, the value is a success code. A failure code means that an error condition triggered the event.


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



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-event-generators">Media Event Generators</a>
 

 

