---
UID: NS:commctrl.tagNMTVSTATEIMAGECHANGING
title: NMTVSTATEIMAGECHANGING (commctrl.h)
author: windows-sdk-content
description: Contains information about an NM_TVSTATEIMAGECHANGING notification code.
old-location: controls\NMTVSTATEIMAGECHANGING.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvstateimagechanging.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPNMTVSTATEIMAGECHANGING, LPNMTVSTATEIMAGECHANGING, LPNMTVSTATEIMAGECHANGING structure pointer [Windows Controls], NMTVSTATEIMAGECHANGING, NMTVSTATEIMAGECHANGING structure [Windows Controls], _shell_NMTVSTATEIMAGECHANGING, _shell_NMTVSTATEIMAGECHANGING_cpp, commctrl/LPNMTVSTATEIMAGECHANGING, commctrl/NMTVSTATEIMAGECHANGING, controls.NMTVSTATEIMAGECHANGING, controls._shell_NMTVSTATEIMAGECHANGING'
ms.topic: struct
f1_keywords:
- commctrl/NMTVSTATEIMAGECHANGING
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
- NMTVSTATEIMAGECHANGING
targetos: Windows
req.typenames: NMTVSTATEIMAGECHANGING, *LPNMTVSTATEIMAGECHANGING
req.redist: 
ms.custom: 19H1
---

# NMTVSTATEIMAGECHANGING structure


## -description


Contains information about an <a href="https://docs.microsoft.com/windows/desktop/Controls/nm-tvstateimagechanging">NM_TVSTATEIMAGECHANGING</a> notification code.


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification code.


### -field hti

Type: <b>HTREEITEM</b>

Handle to the tree-view item whose state image is changing.


### -field iOldStateImageIndex

Type: <b>int</b>

The index of the old state image.


### -field iNewStateImageIndex

Type: <b>int</b>

The index of the new state image.

