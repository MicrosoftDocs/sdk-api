---
UID: NS:commctrl.tagNMLVLINK
title: tagNMLVLINK
author: windows-sdk-content
description: Contains information about an LVN_LINKCLICK notification code.
old-location: controls\NMLVLINK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvlink.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*PNMLVLINK, LPNMLVLINK, LPNMLVLINK structure pointer [Windows Controls], NMLVLINK, NMLVLINK structure [Windows Controls], commctrl/LPNMLVLINK, commctrl/NMLVLINK, controls.NMLVLINK, controls.shell_NMLVLINK, shell_NMLVLINK, shell_NMLVLINK_cpp, tagNMLVLINK"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - NMLVLINK
product: Windows
targetos: Windows
req.typenames: NMLVLINK, *PNMLVLINK
req.redist: 
---

# tagNMLVLINK structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/de8f40d6-b79e-4324-af67-9a3c0915609d">LVN_LINKCLICK</a> notification code.



## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains basic information about the notification code.


### -field link

Type: <b><a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a></b>


<a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a> structure that contains information about the link that was clicked.


### -field iItem

Type: <b>int</b>

Index of the item that contains the link.


### -field iSubItem

Type: <b>int</b>

Subitem, if any. This member may be <b>NULL</b>. For a link in a group header, this is the group identifier, as set in <a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a>.

