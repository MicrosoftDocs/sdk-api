---
UID: NS:commctrl.tagNMLVFINDITEMW
title: tagNMLVFINDITEMW
author: windows-driver-content
description: Contains information the owner needs to find items requested by a virtual list-view control. This structure is used with the LVN_ODFINDITEM notification code.
old-location: controls\NMLVFINDITEM.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvfinditem.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: "*LPNMLVFINDITEMW, NMLVFINDITEM, NMLVFINDITEM structure [Windows Controls], NMLVFINDITEMA, NMLVFINDITEMW, PNMLVFINDITEM, PNMLVFINDITEM structure pointer [Windows Controls], _win32_NMLVFINDITEM, _win32_NMLVFINDITEM_cpp, commctrl/NMLVFINDITEM, commctrl/NMLVFINDITEMA, commctrl/NMLVFINDITEMW, commctrl/PNMLVFINDITEM, controls.NMLVFINDITEM, controls._win32_NMLVFINDITEM, tagNMLVFINDITEMW"
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
req.unicode-ansi: NMLVFINDITEMW (Unicode) and NMLVFINDITEMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NMLVFINDITEMW, *LPNMLVFINDITEMW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMLVFINDITEM
-	NMLVFINDITEMA
-	NMLVFINDITEMW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMLVFINDITEMW structure


## -description


Contains information the owner needs to find items requested by a <a href="List_View_Controls_Overview.htm">virtual list-view</a> control. This structure is used with the <a href="https://msdn.microsoft.com/5a3f9fed-0c57-46bf-b986-ea8b54290b5e">LVN_ODFINDITEM</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information on this notification code. 


### -field iStart

Type: <b>int</b>

Index of the item at which the search will start. 


### -field lvfi

Type: <b><a href="https://msdn.microsoft.com/6d78c0ec-9735-407d-a20b-efb7dc3b0fba">LVFINDINFO</a></b>


<a href="https://msdn.microsoft.com/6d78c0ec-9735-407d-a20b-efb7dc3b0fba">LVFINDINFO</a> structure that contains information necessary to perform a search. 

