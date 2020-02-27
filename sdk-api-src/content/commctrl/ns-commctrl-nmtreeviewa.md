---
UID: NS:commctrl.tagNMTREEVIEWA
title: NMTREEVIEWA (commctrl.h)
description: Contains information about a tree-view notification message. This structure is identical to the NM_TREEVIEW structure, but it has been renamed to follow current naming conventions.
old-location: controls\NMTREEVIEW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtreeview.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTREEVIEWA, LPNMTREEVIEW, LPNMTREEVIEW structure pointer [Windows Controls], NMTREEVIEW, NMTREEVIEW structure [Windows Controls], NMTREEVIEWA, NMTREEVIEWW, _win32_NMTREEVIEW, _win32_NMTREEVIEW_cpp, commctrl/LPNMTREEVIEW, commctrl/NMTREEVIEW, commctrl/NMTREEVIEWA, commctrl/NMTREEVIEWW, controls.NMTREEVIEW, controls._win32_NMTREEVIEW'
f1_keywords:
- commctrl/NMTREEVIEW
dev_langs:
- c++
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
targetos: Windows
req.typenames: NMTREEVIEWA, *LPNMTREEVIEWA
req.redist: 
ms.custom: 19H1
---

# NMTREEVIEWA structure


## -description


Contains information about a tree-view notification message. This structure is identical to the 
			<b>NM_TREEVIEW</b> structure, but it has been renamed to follow current naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification message. 


### -field action

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Notification-specific action flag. This member is used with the following notification codes.

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-itemexpanding">TVN_ITEMEXPANDING</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-itemexpanded">TVN_ITEMEXPANDED</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-selchanging">TVN_SELCHANGING</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-selchanged">TVN_SELCHANGED</a>
</li>
</ul>
For the possible action flag values, see <a href="https://docs.microsoft.com/windows/desktop/Controls/tvm-expand">TVM_EXPAND</a> and <a href="https://docs.microsoft.com/windows/desktop/Controls/tvn-selchanged">TVN_SELCHANGED</a>. 


### -field itemOld

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a> structure that contains information about the old item state. This member is zero for notification messages that do not use it. 


### -field itemNew

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a> structure that contains information about the new item state. This member is zero for notification messages that do not use it. 


### -field ptDrag

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a></b>


<a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that contains the client coordinates of the mouse at the time the event occurred that caused the notification message to be sent. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>
 

 

