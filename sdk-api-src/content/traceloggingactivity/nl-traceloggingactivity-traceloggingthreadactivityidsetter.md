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

# TraceLoggingThreadActivityIdSetter class


## -description


Tags a thread with an activity id so ETW marks all events in that thread with the activity id.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingThreadActivityIdSetter</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingThreadActivityIdSetter</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F950256A-27A8-4C8F-B4A3-974F0E095103">TraceLoggingThreadActivityIdSetter Constructor</a>
</td>
<td align="left" width="63%">
Creates a new <b>TraceLoggingThreadActivityIdSetter</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5B400757-40D7-4DF3-AF9C-C436DE86C7F9">TraceLoggingThreadActivityIDSetter Constructor</a>
</td>
<td align="left" width="63%">
Saves the original activity ID and sets a new activity on the thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5B400757-40D7-4DF3-AF9C-C436DE86C7F9">TraceLoggingThreadActivityIdSetter Destructor</a>
</td>
<td align="left" width="63%">
Restores the original activity ID to the thread.

</td>
</tr>
</table> 


## -remarks




           All activity that occurs in a thread will be tagged with the associated activity id for the life of this object or until a new activity is nested in the thread. That new nested id will take precedence over the <b>TraceLoggingThreadActivityIdSetter</b> object.
         

<div class="alert"><b>Caution</b>  <p class="note">Only use this class when you can guarantee that all activities for this thread are fully nested. In DEBUG builds, the class will raise an assertion during its Stop event, if it detects incorrect activity nesting, or if the Stop event occurs on a thread other than the thread used to start it.

</div>
<div> </div>


