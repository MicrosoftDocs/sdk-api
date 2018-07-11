---
UID: NF:imapi2.DDiscFormat2DataEvents.Update
title: DDiscFormat2DataEvents::Update
author: windows-sdk-content
description: Implement this method to receive progress notification of the current write operation.
old-location: imapi\ddiscformat2dataevents_update.htm
old-project: imapi
ms.assetid: 786fc936-9493-4cc3-a937-4d1f4b54fe88
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: DDiscFormat2DataEvents interface [IMAPI],Update method, DDiscFormat2DataEvents.Update, DDiscFormat2DataEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DDiscFormat2DataEvents interface, imapi.ddiscformat2dataevents_update, imapi2/DDiscFormat2DataEvents::Update
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscFormat2DataEvents.Update
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DDiscFormat2DataEvents::Update


## -description


Implement this method to receive progress notification of the current write operation. 


## -parameters




### -param object [in]

The <a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a> interface that initiated the write operation. 

This parameter is a <b>MsftDiscFormat2Data</b> object in script.


### -param progress [in]

An <a href="https://msdn.microsoft.com/6bf149d3-62ea-4ef5-8d45-44df9ad4982c">IDiscFormat2DataEventArgs</a> interface that you use to determine the progress of the write operation. 

This parameter is a <b>MsftDiscFormat2Data</b> object in script.


## -returns



Return values are ignored.




## -remarks



Notifications are sent in response to calling the <a href="https://msdn.microsoft.com/9daf31f3-84c2-48b2-ab21-a3809b6ed9af">IDiscFormat2Data::Write</a> method.

Notification is sent when the current action changes:

<ul>
<li>Once when initializing the hardware</li>
<li>Once when calibrating the power</li>
<li>Once when formatting the media, if required by the media type</li>
<li>Every 0.5 seconds during the write operation</li>
<li>Once after the operation completes</li>
</ul>
To stop the write process, call the <a href="https://msdn.microsoft.com/0fe5705e-7f48-4a4e-a535-a3dd105a6139">IDiscFormat2Data::CancelWrite</a> method.




## -see-also




<a href="https://msdn.microsoft.com/f9f1d976-9ec9-40a5-92b6-d00a7e15d0aa">DDiscFormat2DataEvents</a>



<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>
 

 

