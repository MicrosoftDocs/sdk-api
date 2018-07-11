---
UID: NS:commctrl.tagNMTVSTATEIMAGECHANGING
title: tagNMTVSTATEIMAGECHANGING
author: windows-sdk-content
description: Contains information about an NM_TVSTATEIMAGECHANGING notification code.
old-location: controls\NMTVSTATEIMAGECHANGING.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvstateimagechanging.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: "*LPNMTVSTATEIMAGECHANGING, LPNMTVSTATEIMAGECHANGING, LPNMTVSTATEIMAGECHANGING structure pointer [Windows Controls], NMTVSTATEIMAGECHANGING, NMTVSTATEIMAGECHANGING structure [Windows Controls], _shell_NMTVSTATEIMAGECHANGING, _shell_NMTVSTATEIMAGECHANGING_cpp, commctrl/LPNMTVSTATEIMAGECHANGING, commctrl/NMTVSTATEIMAGECHANGING, controls.NMTVSTATEIMAGECHANGING, controls._shell_NMTVSTATEIMAGECHANGING, tagNMTVSTATEIMAGECHANGING"
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
tech.root: 
req.typenames: NMTVSTATEIMAGECHANGING, *LPNMTVSTATEIMAGECHANGING
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
req.lib: 
req.dll: 
req.irql: 
---

# tagNMTVSTATEIMAGECHANGING structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/8e42d8b3-5e76-4d03-94b0-3e4583669095">NM_TVSTATEIMAGECHANGING</a> notification code.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification code.


### -field hti

Type: <b>HTREEITEM</b>

Handle to the tree-view item whose state image is changing.


### -field iOldStateImageIndex

Type: <b>int</b>

The index of the old state image.


### -field iNewStateImageIndex

Type: <b>int</b>

The index of the new state image.

