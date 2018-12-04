---
UID: NS:commctrl.tagNMTREEVIEWW
title: tagNMTREEVIEWW
author: windows-sdk-content
description: Contains information about a tree-view notification message. This structure is identical to the NM_TREEVIEW structure, but it has been renamed to follow current naming conventions.
old-location: controls\NMTREEVIEW.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtreeview.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPNMTREEVIEWW, LPNMTREEVIEW, LPNMTREEVIEW structure pointer [Windows Controls], NMTREEVIEW, NMTREEVIEW structure [Windows Controls], NMTREEVIEWA, NMTREEVIEWW, _win32_NMTREEVIEW, _win32_NMTREEVIEW_cpp, commctrl/LPNMTREEVIEW, commctrl/NMTREEVIEW, commctrl/NMTREEVIEWA, commctrl/NMTREEVIEWW, controls.NMTREEVIEW, controls._win32_NMTREEVIEW, tagNMTREEVIEWW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMTREEVIEWW (Unicode) and NMTREEVIEWA (ANSI)
req.idl: 
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
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMTREEVIEW
 - NMTREEVIEWA
 - NMTREEVIEWW
product: Windows
targetos: Windows
req.typenames: NMTREEVIEWW, *LPNMTREEVIEWW
req.redist: 
---

# tagNMTREEVIEWW structure


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

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>


<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the client coordinates of the mouse at the time the event occurred that caused the notification message to be sent. 


## -see-also




<a href="https://msdn.microsoft.com/23ff9dc1-3d92-4e94-8df5-7a645039ce27">WM_NOTIFY</a>
 

 

