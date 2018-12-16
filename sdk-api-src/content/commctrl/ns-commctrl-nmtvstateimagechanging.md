---
UID: NS:commctrl.tagNMTVSTATEIMAGECHANGING
title: NMTVSTATEIMAGECHANGING
author: windows-sdk-content
description: Contains information about an NM_TVSTATEIMAGECHANGING notification code.
old-location: controls\NMTVSTATEIMAGECHANGING.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvstateimagechanging.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNMTVSTATEIMAGECHANGING, LPNMTVSTATEIMAGECHANGING, LPNMTVSTATEIMAGECHANGING structure pointer [Windows Controls], NMTVSTATEIMAGECHANGING, NMTVSTATEIMAGECHANGING structure [Windows Controls], _shell_NMTVSTATEIMAGECHANGING, _shell_NMTVSTATEIMAGECHANGING_cpp, commctrl/LPNMTVSTATEIMAGECHANGING, commctrl/NMTVSTATEIMAGECHANGING, controls.NMTVSTATEIMAGECHANGING, controls._shell_NMTVSTATEIMAGECHANGING"
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
 - NMTVSTATEIMAGECHANGING
product: Windows
targetos: Windows
req.typenames: NMTVSTATEIMAGECHANGING, *LPNMTVSTATEIMAGECHANGING
req.redist: 
---

# NMTVSTATEIMAGECHANGING structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/en-us/library/Bb775572(v=VS.85).aspx">NM_TVSTATEIMAGECHANGING</a> notification code.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification code.


### -field hti

Type: <b>HTREEITEM</b>

Handle to the tree-view item whose state image is changing.


### -field iOldStateImageIndex

Type: <b>int</b>

The index of the old state image.


### -field iNewStateImageIndex

Type: <b>int</b>

The index of the new state image.

