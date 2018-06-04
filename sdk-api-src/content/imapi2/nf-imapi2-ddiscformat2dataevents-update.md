---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

