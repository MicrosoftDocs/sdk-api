---
UID: NS:commctrl.tagNMLVLINK
title: NMLVLINK (commctrl.h)
author: windows-sdk-content
description: Contains information about an LVN_LINKCLICK notification code.
old-location: controls\NMLVLINK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvlink.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PNMLVLINK, LPNMLVLINK, LPNMLVLINK structure pointer [Windows Controls], NMLVLINK, NMLVLINK structure [Windows Controls], commctrl/LPNMLVLINK, commctrl/NMLVLINK, controls.NMLVLINK, controls.shell_NMLVLINK, shell_NMLVLINK, shell_NMLVLINK_cpp"
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
ms.custom: 19H1
---

# NMLVLINK structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/en-us/library/Bb774851(v=VS.85).aspx">LVN_LINKCLICK</a> notification code.



## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains basic information about the notification code.


### -field link

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb760710(v=VS.85).aspx">LITEM</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb760710(v=VS.85).aspx">LITEM</a> structure that contains information about the link that was clicked.


### -field iItem

Type: <b>int</b>

Index of the item that contains the link.


### -field iSubItem

Type: <b>int</b>

Subitem, if any. This member may be <b>NULL</b>. For a link in a group header, this is the group identifier, as set in <a href="https://msdn.microsoft.com/en-us/library/Bb774769(v=VS.85).aspx">LVGROUP</a>.

