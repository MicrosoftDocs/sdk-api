---
UID: NS:commctrl.tagNMLVFINDITEMW
title: NMLVFINDITEMW
author: windows-sdk-content
description: Contains information the owner needs to find items requested by a virtual list-view control. This structure is used with the LVN_ODFINDITEM notification code.
old-location: controls\NMLVFINDITEM.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvfinditem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNMLVFINDITEMW, NMLVFINDITEM, NMLVFINDITEM structure [Windows Controls], NMLVFINDITEMA, NMLVFINDITEMW, PNMLVFINDITEM, PNMLVFINDITEM structure pointer [Windows Controls], _win32_NMLVFINDITEM, _win32_NMLVFINDITEM_cpp, commctrl/NMLVFINDITEM, commctrl/NMLVFINDITEMA, commctrl/NMLVFINDITEMW, commctrl/PNMLVFINDITEM, controls.NMLVFINDITEM, controls._win32_NMLVFINDITEM"
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMLVFINDITEMW (Unicode) and NMLVFINDITEMA (ANSI)
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
 - NMLVFINDITEM
 - NMLVFINDITEMA
 - NMLVFINDITEMW
product: Windows
targetos: Windows
req.typenames: NMLVFINDITEMW, *LPNMLVFINDITEMW
req.redist: 
---

# NMLVFINDITEMW structure


## -description


Contains information the owner needs to find items requested by a <a href="https://msdn.microsoft.com/en-us/library/Bb774735(v=VS.85).aspx">virtual list-view</a> control. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb774857(v=VS.85).aspx">LVN_ODFINDITEM</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information on this notification code. 


### -field iStart

Type: <b>int</b>

Index of the item at which the search will start. 


### -field lvfi

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774745(v=VS.85).aspx">LVFINDINFO</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb774745(v=VS.85).aspx">LVFINDINFO</a> structure that contains information necessary to perform a search. 

