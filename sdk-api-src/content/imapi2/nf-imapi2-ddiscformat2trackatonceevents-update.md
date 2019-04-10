---
UID: NF:imapi2.DDiscFormat2TrackAtOnceEvents.Update
title: DDiscFormat2TrackAtOnceEvents::Update (imapi2.h)
author: windows-sdk-content
description: Implement this method to receive progress notification of the current track-writing operation.
old-location: imapi\ddiscformat2trackatonceevents_update.htm
tech.root: imapi
ms.assetid: d63ff41d-993c-4f42-a4a3-f7c67f292a03
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DDiscFormat2TrackAtOnceEvents interface [IMAPI],Update method, DDiscFormat2TrackAtOnceEvents.Update, DDiscFormat2TrackAtOnceEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DDiscFormat2TrackAtOnceEvents interface, imapi.ddiscformat2trackatonceevents_update, imapi2/DDiscFormat2TrackAtOnceEvents::Update
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscFormat2TrackAtOnceEvents.Update
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DDiscFormat2TrackAtOnceEvents::Update


## -description


Implement this method to receive progress notification of the current track-writing operation.


## -parameters




### -param object [in]

The <a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a> interface that initiated the write operation. 

This parameter is a <b>MsftDiscFormat2TrackAtOnce</b> object in script.


### -param progress [in]

An <a href="https://msdn.microsoft.com/4bbcc3e1-0c85-4ed8-bbf6-e172e5896ed9">IDiscFormat2TrackAtOnceEventArgs</a> interface that you use to determine the progress of the write operation. 

This parameter is a <b>MsftDiscFormat2TrackAtOnce</b> object in script.


## -returns



Return values are ignored.




## -remarks



Notifications are sent in response to calling the <a href="https://msdn.microsoft.com/3ac74b91-b0c7-471f-b6a9-1393d677e0c1">IDiscFormat2TrackAtOnce::AddAudioTrack</a> method.

To stop the write process, call the <a href="https://msdn.microsoft.com/09e71d36-da1d-4ba0-bd6b-4ce4425d481a">IDiscFormat2TrackAtOnce::CancelAddTrack</a> method.




## -see-also




<a href="https://msdn.microsoft.com/15d88768-f6e9-4d0a-a132-08f89fb3c34f">DDiscFormat2TrackAtOnceEvents</a>



<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/09e71d36-da1d-4ba0-bd6b-4ce4425d481a">IDiscFormat2TrackAtOnce::CancelAddTrack</a>
 

 

