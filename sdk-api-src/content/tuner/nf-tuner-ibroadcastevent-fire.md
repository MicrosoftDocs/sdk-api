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

# IBroadcastEvent::Fire


## -description



The <b>Fire</b> method fires a broadcast event.




## -parameters




### -param EventID

GUID that specifies the event.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



For television tuning, the following event is defined.

<table>
<tr>
<th>
              Tuner Event
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>EVENTID_TuningChanged</td>
<td>Fired when the tuner changes stations or channels. Defined in Bdamedia.h.</td>
</tr>
</table>
 

For a list of events fired by the TV ratings components, see <a href="https://msdn.microsoft.com/73a6a4fd-cca2-4143-91f9-37f4f6d952b8">TV Ratings Broadcast Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent Interface</a>



<a href="https://msdn.microsoft.com/73a6a4fd-cca2-4143-91f9-37f4f6d952b8">TV Ratings Broadcast Events</a>
 

 

