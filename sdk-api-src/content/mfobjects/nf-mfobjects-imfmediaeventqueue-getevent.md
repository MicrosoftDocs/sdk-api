---
UID: NF:mfobjects.IMFMediaEventQueue.GetEvent
title: IMFMediaEventQueue::GetEvent (mfobjects.h)
author: windows-sdk-content
description: Retrieves the next event in the queue. This method is synchronous.Call this method inside your implementation of IMFMediaEventGenerator::GetEvent. Pass the parameters from that method directly to this method.
old-location: mf\imfmediaeventqueue_getevent.htm
tech.root: medfound
ms.assetid: b7c48607-f410-47ee-8cc6-38123919da55
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEvent, GetEvent method [Media Foundation], GetEvent method [Media Foundation],IMFMediaEventQueue interface, IMFMediaEventQueue interface [Media Foundation],GetEvent method, IMFMediaEventQueue.GetEvent, IMFMediaEventQueue::GetEvent, b7c48607-f410-47ee-8cc6-38123919da55, mf.imfmediaeventqueue_getevent, mfobjects/IMFMediaEventQueue::GetEvent
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
 - IMFMediaEventQueue.GetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEventQueue::GetEvent


## -description



Retrieves the next event in the queue. This method is synchronous.

Call this method inside your implementation of <a href="https://msdn.microsoft.com/e78464b5-ec6b-4739-a135-352fa297916a">IMFMediaEventGenerator::GetEvent</a>. Pass the parameters from that method directly to this method.




## -parameters




### -param dwFlags [in]

Specifies whether the method blocks until an event is queued. For a list of valid flags, see <a href="https://msdn.microsoft.com/e78464b5-ec6b-4739-a135-352fa297916a">IMFMediaEventGenerator::GetEvent</a>.


### -param ppEvent [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface.


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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/6ec52973-0d90-463b-b2be-08d5d6fdcc05">Shutdown</a> method was called.

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




<a href="https://msdn.microsoft.com/e1698caa-db70-436d-af6a-64c6e7247590">IMFMediaEventQueue</a>
 

 

