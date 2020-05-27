---
UID: NS:commctrl.tagNMLISTVIEW
title: NMLISTVIEW (commctrl.h)
description: Contains information about a list-view notification message. This structure is the same as the NM_LISTVIEW structure but has been renamed to fit standard naming conventions.
helpviewer_keywords: ["*LPNMLISTVIEW","LPNMLISTVIEW","LPNMLISTVIEW structure pointer [Windows Controls]","NMLISTVIEW","NMLISTVIEW structure [Windows Controls]","_win32_NMLISTVIEW","_win32_NMLISTVIEW_cpp","commctrl/LPNMLISTVIEW","commctrl/NMLISTVIEW","controls.NMLISTVIEW","controls._win32_NMLISTVIEW"]
old-location: controls\NMLISTVIEW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlistview.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMLISTVIEW, LPNMLISTVIEW, LPNMLISTVIEW structure pointer [Windows Controls], NMLISTVIEW, NMLISTVIEW structure [Windows Controls], _win32_NMLISTVIEW, _win32_NMLISTVIEW_cpp, commctrl/LPNMLISTVIEW, commctrl/NMLISTVIEW, controls.NMLISTVIEW, controls._win32_NMLISTVIEW'
f1_keywords:
- commctrl/NMLISTVIEW
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
req.unicode-ansi: 
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
- NMLISTVIEW
targetos: Windows
req.typenames: NMLISTVIEW, *LPNMLISTVIEW
req.redist: 
ms.custom: 19H1
---

# NMLISTVIEW structure


## -description


Contains information about a list-view notification message. This structure is the same as the <b>NM_LISTVIEW</b> structure but has been renamed to fit standard naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification message. 


### -field iItem

Type: <b>int</b>

Identifies the list-view item, or -1 if not used. 


### -field iSubItem

Type: <b>int</b>

Identifies the subitem, or zero if none. 


### -field uNewState

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

New item state. This member is zero for notification messages that do not use it. For a list of possible values, see <a href="https://docs.microsoft.com/windows/desktop/Controls/list-view-item-states">List-View Item States</a>. 


### -field uOldState

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Old item state. This member is zero for notification messages that do not use it. For a list of possible values, see <a href="https://docs.microsoft.com/windows/desktop/Controls/list-view-item-states">List-View Item States</a>.


### -field uChanged

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Set of flags that indicate the item attributes that have changed. This member is zero for notifications that do not use it. Otherwise, it can have the same values as the 
					<b>mask</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure. 


### -field ptAction

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a></b>


<a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that indicates the location at which the event occurred. This member is undefined for notification messages that do not use it. 


### -field lParam

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined value of the item. This member is undefined for notification messages that do not use it. 

