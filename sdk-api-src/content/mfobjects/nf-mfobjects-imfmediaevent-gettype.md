---
UID: NF:mfobjects.IMFMediaEvent.GetType
title: IMFMediaEvent::GetType (mfobjects.h)
author: windows-sdk-content
description: Retrieves the event type. The event type indicates what happened to trigger the event. It also defines the meaning of the event value.
old-location: mf\imfmediaevent_gettype.htm
tech.root: medfound
ms.assetid: b62e0d9f-dada-4b75-a8d3-568ee2955888
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Media Foundation], GetType method [Media Foundation],IMFMediaEvent interface, IMFMediaEvent interface [Media Foundation],GetType method, IMFMediaEvent.GetType, IMFMediaEvent::GetType, b62e0d9f-dada-4b75-a8d3-568ee2955888, mf.imfmediaevent_gettype, mfobjects/IMFMediaEvent::GetType
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
 - IMFMediaEvent.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEvent::GetType


## -description



Retrieves the event type. The event type indicates what happened to trigger the event. It also defines the meaning of the event value.




## -parameters




### -param pmet [out]

Receives the event type. For a list of event types, see <a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-events">Media Foundation Events</a>.


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
 

 

