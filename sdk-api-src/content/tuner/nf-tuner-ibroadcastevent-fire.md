---
UID: NF:tuner.IBroadcastEvent.Fire
title: IBroadcastEvent::Fire (tuner.h)
description: The Fire method fires a broadcast event.
helpviewer_keywords: ["Fire","Fire method [Microsoft TV Technologies]","Fire method [Microsoft TV Technologies]","IBroadcastEvent interface","IBroadcastEvent interface [Microsoft TV Technologies]","Fire method","IBroadcastEvent.Fire","IBroadcastEvent::Fire","IBroadcastEventFire","mstv.ibroadcastevent_fire","tuner/IBroadcastEvent::Fire"]
old-location: mstv\ibroadcastevent_fire.htm
tech.root: mstv
ms.assetid: 974b42d7-bf68-426b-a146-4e520cac3274
ms.date: 12/05/2018
ms.keywords: Fire, Fire method [Microsoft TV Technologies], Fire method [Microsoft TV Technologies],IBroadcastEvent interface, IBroadcastEvent interface [Microsoft TV Technologies],Fire method, IBroadcastEvent.Fire, IBroadcastEvent::Fire, IBroadcastEventFire, mstv.ibroadcastevent_fire, tuner/IBroadcastEvent::Fire
f1_keywords:
- tuner/IBroadcastEvent.Fire
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- IBroadcastEvent.Fire
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBroadcastEvent::Fire


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]



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
<th>Tuner Event
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>EVENTID_TuningChanged</td>
<td>Fired when the tuner changes stations or channels. Defined in Bdamedia.h.</td>
</tr>
</table>
 

For a list of events fired by the TV ratings components, see <a href="/previous-versions/windows/desktop/mstv/tv-ratings-broadcast-events">TV Ratings Broadcast Events</a>.




## -see-also




<a href="/previous-versions/dd376294(v=vs.85)">IBroadcastEvent Interface</a>



<a href="/previous-versions/windows/desktop/mstv/tv-ratings-broadcast-events">TV Ratings Broadcast Events</a>
 

 