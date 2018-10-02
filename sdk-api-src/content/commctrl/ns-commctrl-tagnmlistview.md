---
UID: NS:commctrl.tagNMLISTVIEW
title: tagNMLISTVIEW
author: windows-sdk-content
description: Contains information about a list-view notification message. This structure is the same as the NM_LISTVIEW structure but has been renamed to fit standard naming conventions.
old-location: controls\NMLISTVIEW.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlistview.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPNMLISTVIEW, LPNMLISTVIEW, LPNMLISTVIEW structure pointer [Windows Controls], NMLISTVIEW, NMLISTVIEW structure [Windows Controls], _win32_NMLISTVIEW, _win32_NMLISTVIEW_cpp, commctrl/LPNMLISTVIEW, commctrl/NMLISTVIEW, controls.NMLISTVIEW, controls._win32_NMLISTVIEW, tagNMLISTVIEW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: NMLISTVIEW, *LPNMLISTVIEW
req.redist: 
---

# tagNMLISTVIEW structure


## -description


Contains information about a list-view notification message. This structure is the same as the <b>NM_LISTVIEW</b> structure but has been renamed to fit standard naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification message. 


### -field iItem

Type: <b>int</b>

Identifies the list-view item, or -1 if not used. 


### -field iSubItem

Type: <b>int</b>

Identifies the subitem, or zero if none. 


### -field uNewState

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

New item state. This member is zero for notification messages that do not use it. For a list of possible values, see <a href="https://msdn.microsoft.com/en-us/library/Bb774733(v=VS.85).aspx">List-View Item States</a>. 


### -field uOldState

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Old item state. This member is zero for notification messages that do not use it. For a list of possible values, see <a href="https://msdn.microsoft.com/en-us/library/Bb774733(v=VS.85).aspx">List-View Item States</a>.


### -field uChanged

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Set of flags that indicate the item attributes that have changed. This member is zero for notifications that do not use it. Otherwise, it can have the same values as the 
					<b>mask</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb774760(v=VS.85).aspx">LVITEM</a> structure. 


### -field ptAction

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>


<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that indicates the location at which the event occurred. This member is undefined for notification messages that do not use it. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPARAM</a></b>

Application-defined value of the item. This member is undefined for notification messages that do not use it. 

