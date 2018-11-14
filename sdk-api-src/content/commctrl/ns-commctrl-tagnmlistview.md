---
UID: NS:commctrl.tagNMLISTVIEW
title: tagNMLISTVIEW
author: windows-sdk-content
description: Contains information about a list-view notification message. This structure is the same as the NM_LISTVIEW structure but has been renamed to fit standard naming conventions.
old-location: controls\NMLISTVIEW.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlistview.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPNMLISTVIEW, LPNMLISTVIEW, LPNMLISTVIEW structure pointer [Windows Controls], NMLISTVIEW, NMLISTVIEW structure [Windows Controls], _win32_NMLISTVIEW, _win32_NMLISTVIEW_cpp, commctrl/LPNMLISTVIEW, commctrl/NMLISTVIEW, controls.NMLISTVIEW, controls._win32_NMLISTVIEW, tagNMLISTVIEW"
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

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification message. 


### -field iItem

Type: <b>int</b>

Identifies the list-view item, or -1 if not used. 


### -field iSubItem

Type: <b>int</b>

Identifies the subitem, or zero if none. 


### -field uNewState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

New item state. This member is zero for notification messages that do not use it. For a list of possible values, see <a href="https://msdn.microsoft.com/21827f4a-f133-489b-bbd2-6979d1928b40">List-View Item States</a>. 


### -field uOldState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Old item state. This member is zero for notification messages that do not use it. For a list of possible values, see <a href="https://msdn.microsoft.com/21827f4a-f133-489b-bbd2-6979d1928b40">List-View Item States</a>.


### -field uChanged

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Set of flags that indicate the item attributes that have changed. This member is zero for notifications that do not use it. Otherwise, it can have the same values as the 
					<b>mask</b> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure. 


### -field ptAction

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>


<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that indicates the location at which the event occurred. This member is undefined for notification messages that do not use it. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Application-defined value of the item. This member is undefined for notification messages that do not use it. 

