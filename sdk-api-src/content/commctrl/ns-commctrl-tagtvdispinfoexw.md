---
UID: NS:commctrl.tagTVDISPINFOEXW
title: tagTVDISPINFOEXW
author: windows-sdk-content
description: Contains information pertaining to extended TreeView notification information.
old-location: controls\NMTVDISPINFOEX.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvdispinfoex.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*LPNMTVDISPINFOEXW, LPNMTVDISPINFOEX, LPNMTVDISPINFOEX structure pointer [Windows Controls], NMTVDISPINFOEX, NMTVDISPINFOEX structure [Windows Controls], NMTVDISPINFOEXA, NMTVDISPINFOEXW, _shell_NMTVDISPINFOEX, _shell_NMTVDISPINFOEX_cpp, commctrl/LPNMTVDISPINFOEX, commctrl/NMTVDISPINFOEX, commctrl/NMTVDISPINFOEXA, commctrl/NMTVDISPINFOEXW, controls.NMTVDISPINFOEX, controls._shell_NMTVDISPINFOEX, tagTVDISPINFOEXW"
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
req.unicode-ansi: NMTVDISPINFOEXW (Unicode) and NMTVDISPINFOEXA (ANSI)
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
 - NMTVDISPINFOEX
 - NMTVDISPINFOEXA
 - NMTVDISPINFOEXW
product: Windows
targetos: Windows
req.typenames: NMTVDISPINFOEXW, *LPNMTVDISPINFOEXW
req.redist: 
---

# tagTVDISPINFOEXW structure


## -description


Contains information pertaining to extended TreeView notification information.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification.


### -field item

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb773459(v=VS.85).aspx">TVITEMEX</a></b>

Specifies or receives attributes of a TreeView item.

