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

# tagNMTREEVIEWA structure


## -description


Contains information about a tree-view notification message. This structure is identical to the 
			<b>NM_TREEVIEW</b> structure, but it has been renamed to follow current naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification message. 


### -field action

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Notification-specific action flag. This member is used with the following notification codes.

<ul>
<li>
<a href="https://msdn.microsoft.com/5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec">TVN_ITEMEXPANDING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/18d9d61d-6ec5-4d3b-9c02-36d0e61ed232">TVN_ITEMEXPANDED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/53f24ee0-433c-4680-9075-5e2b21117ed9">TVN_SELCHANGING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/682170d3-5843-4d92-afeb-c37f3502ed5d">TVN_SELCHANGED</a>
</li>
</ul>
For the possible action flag values, see <a href="https://msdn.microsoft.com/d6c2e5b2-ce36-4c2b-b527-91c6de56e305">TVM_EXPAND</a> and <a href="https://msdn.microsoft.com/682170d3-5843-4d92-afeb-c37f3502ed5d">TVN_SELCHANGED</a>. 


### -field itemOld

Type: <b><a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a></b>


<a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a> structure that contains information about the old item state. This member is zero for notification messages that do not use it. 


### -field itemNew

Type: <b><a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a></b>


<a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a> structure that contains information about the new item state. This member is zero for notification messages that do not use it. 


### -field ptDrag

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that contains the client coordinates of the mouse at the time the event occurred that caused the notification message to be sent. 


## -see-also




<a href="https://msdn.microsoft.com/23ff9dc1-3d92-4e94-8df5-7a645039ce27">WM_NOTIFY</a>
 

 

