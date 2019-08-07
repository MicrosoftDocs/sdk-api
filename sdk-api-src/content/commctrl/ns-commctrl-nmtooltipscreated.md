---
UID: NS:commctrl.tagNMTOOLTIPSCREATED
title: NMTOOLTIPSCREATED (commctrl.h)
author: windows-sdk-content
description: Contains information used with NM_TOOLTIPSCREATED notification codes.
old-location: controls\NMTOOLTIPSCREATED.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmtooltipscreated.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPNMTOOLTIPSCREATED, LPNMTOOLTIPSCREATED, LPNMTOOLTIPSCREATED structure pointer [Windows Controls], NMTOOLTIPSCREATED, NMTOOLTIPSCREATED structure [Windows Controls], _win32_NMTOOLTIPSCREATED, _win32_NMTOOLTIPSCREATED_cpp, commctrl/LPNMTOOLTIPSCREATED, commctrl/NMTOOLTIPSCREATED, controls.NMTOOLTIPSCREATED, controls._win32_NMTOOLTIPSCREATED'
ms.topic: struct
f1_keywords:
- commctrl/NMTOOLTIPSCREATED
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
- NMTOOLTIPSCREATED
product: Windows
targetos: Windows
req.typenames: NMTOOLTIPSCREATED, *LPNMTOOLTIPSCREATED
req.redist: 
ms.custom: 19H1
---

# NMTOOLTIPSCREATED structure


## -description


Contains information used with <a href="https://docs.microsoft.com/windows/desktop/Controls/nm-tooltipscreated">NM_TOOLTIPSCREATED</a> notification codes. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about this notification. 


### -field hwndToolTips

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The window handle to the tooltip control created. 

