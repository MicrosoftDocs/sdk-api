---
UID: NF:strmif.IMediaEventSink.Notify
title: IMediaEventSink::Notify
author: windows-sdk-content
description: The Notify method notifies the Filter Graph Manager of an event.
old-location: dshow\imediaeventsink_notify.htm
old-project: DirectShow
ms.assetid: 331f8d58-c7c6-40dd-88ca-5678c7b8c8f1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IMediaEventSink interface [DirectShow],Notify method, IMediaEventSink.Notify, IMediaEventSink::Notify, IMediaEventSinkNotify, Notify, Notify method [DirectShow], Notify method [DirectShow],IMediaEventSink interface, dshow.imediaeventsink_notify, strmif/IMediaEventSink::Notify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaEventSink.Notify
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaEventSink::Notify


## -description



The <code>Notify</code> method notifies the Filter Graph Manager of an event.




## -parameters




### -param EventCode [in]

Identifier of the event.


### -param EventParam1 [in]

First event parameter.


### -param EventParam2 [in]

Second event parameter.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The event is queued but not delivered to the application on this thread. For a list of notification codes and event parameter values, see <a href="https://msdn.microsoft.com/339ffcd9-7724-4c92-b241-afbed81d9380">Event Notification Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/50aa04b4-9a04-4d0d-a558-42595a69aef7">IMediaEventSink Interface</a>
 

 

