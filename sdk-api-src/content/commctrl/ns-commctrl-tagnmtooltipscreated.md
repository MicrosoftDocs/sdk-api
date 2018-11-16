---
UID: NS:commctrl.tagNMTOOLTIPSCREATED
title: tagNMTOOLTIPSCREATED
author: windows-sdk-content
description: Contains information used with NM_TOOLTIPSCREATED notification codes.
old-location: controls\NMTOOLTIPSCREATED.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmtooltipscreated.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPNMTOOLTIPSCREATED, LPNMTOOLTIPSCREATED, LPNMTOOLTIPSCREATED structure pointer [Windows Controls], NMTOOLTIPSCREATED, NMTOOLTIPSCREATED structure [Windows Controls], _win32_NMTOOLTIPSCREATED, _win32_NMTOOLTIPSCREATED_cpp, commctrl/LPNMTOOLTIPSCREATED, commctrl/NMTOOLTIPSCREATED, controls.NMTOOLTIPSCREATED, controls._win32_NMTOOLTIPSCREATED, tagNMTOOLTIPSCREATED"
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
 - NMTOOLTIPSCREATED
product: Windows
targetos: Windows
req.typenames: NMTOOLTIPSCREATED, *LPNMTOOLTIPSCREATED
req.redist: 
---

# tagNMTOOLTIPSCREATED structure


## -description


Contains information used with <a href="https://msdn.microsoft.com/en-us/library/Bb775570(v=VS.85).aspx">NM_TOOLTIPSCREATED</a> notification codes. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about this notification. 


### -field hwndToolTips

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The window handle to the tooltip control created. 

