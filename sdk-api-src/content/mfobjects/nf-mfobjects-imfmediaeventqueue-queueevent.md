---
UID: NF:mfobjects.IMFMediaEventQueue.QueueEvent
title: IMFMediaEventQueue::QueueEvent
author: windows-driver-content
description: Puts an event in the queue.
old-location: mf\imfmediaeventqueue_queueevent.htm
old-project: medfound
ms.assetid: eb04ce9f-fb64-438f-ad4d-ba1fb849d59c
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IMFMediaEventQueue interface [Media Foundation],QueueEvent method, IMFMediaEventQueue.QueueEvent, IMFMediaEventQueue::QueueEvent, QueueEvent, QueueEvent method [Media Foundation], QueueEvent method [Media Foundation],IMFMediaEventQueue interface, eb04ce9f-fb64-438f-ad4d-ba1fb849d59c, mf.imfmediaeventqueue_queueevent, mfobjects/IMFMediaEventQueue::QueueEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaEventQueue.QueueEvent
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEventQueue::QueueEvent


## -description



Puts an event in the queue.




## -parameters




### -param pEvent [in]

Pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface of the event to be put in the queue.


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
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



Call this method when your component needs to raise an event that contains attributes. To create the event object, call <a href="https://msdn.microsoft.com/64da695e-5f56-4f23-9a06-0b0c358e3cc3">MFCreateMediaEvent</a>. Add attributes to the event by using methods from the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. (The <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface inherits <b>IMFAttributes</b>.)

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e1698caa-db70-436d-af6a-64c6e7247590">IMFMediaEventQueue</a>
 

 

