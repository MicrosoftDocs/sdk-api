---
UID: NF:tuner.IBroadcastEvent.Fire
title: IBroadcastEvent::Fire
author: windows-driver-content
description: The Fire method fires a broadcast event.
old-location: mstv\ibroadcastevent_fire.htm
old-project: mstv
ms.assetid: 974b42d7-bf68-426b-a146-4e520cac3274
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: Fire, Fire method [Microsoft TV Technologies], Fire method [Microsoft TV Technologies],IBroadcastEvent interface, IBroadcastEvent interface [Microsoft TV Technologies],Fire method, IBroadcastEvent.Fire, IBroadcastEvent::Fire, IBroadcastEventFire, mstv.ibroadcastevent_fire, tuner/IBroadcastEvent::Fire
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IBroadcastEvent.Fire
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

