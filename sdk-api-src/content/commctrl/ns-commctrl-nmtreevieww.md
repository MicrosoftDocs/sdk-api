---
UID: NS:commctrl.tagNMTREEVIEWW
title: NMTREEVIEWW (commctrl.h)
author: windows-sdk-content
description: Contains information about a tree-view notification message. This structure is identical to the NM_TREEVIEW structure, but it has been renamed to follow current naming conventions.
old-location: controls\NMTREEVIEW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtreeview.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPNMTREEVIEWW, LPNMTREEVIEW, LPNMTREEVIEW structure pointer [Windows Controls], NMTREEVIEW, NMTREEVIEW structure [Windows Controls], NMTREEVIEWA, NMTREEVIEWW, _win32_NMTREEVIEW, _win32_NMTREEVIEW_cpp, commctrl/LPNMTREEVIEW, commctrl/NMTREEVIEW, commctrl/NMTREEVIEWA, commctrl/NMTREEVIEWW, controls.NMTREEVIEW, controls._win32_NMTREEVIEW"
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
ms.custom: 19H1
---

# NMTREEVIEWW structure


## -description


Contains information about a tree-view notification message. This structure is identical to the 
			<b>NM_TREEVIEW</b> structure, but it has been renamed to follow current naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification message. 


### -field action

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Notification-specific action flag. This member is used with the following notification codes.

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb773537(v=VS.85).aspx">TVN_ITEMEXPANDING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb773533(v=VS.85).aspx">TVN_ITEMEXPANDED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb773547(v=VS.85).aspx">TVN_SELCHANGING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb773544(v=VS.85).aspx">TVN_SELCHANGED</a>
</li>
</ul>
For the possible action flag values, see <a href="https://msdn.microsoft.com/en-us/library/Bb773568(v=VS.85).aspx">TVM_EXPAND</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb773544(v=VS.85).aspx">TVN_SELCHANGED</a>. 


### -field itemOld

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a> structure that contains information about the old item state. This member is zero for notification messages that do not use it. 


### -field itemNew

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a> structure that contains information about the new item state. This member is zero for notification messages that do not use it. 


### -field ptDrag

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>


<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the client coordinates of the mouse at the time the event occurred that caused the notification message to be sent. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775583(v=VS.85).aspx">WM_NOTIFY</a>
 

 

