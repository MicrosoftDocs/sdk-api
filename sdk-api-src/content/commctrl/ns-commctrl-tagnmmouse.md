---
UID: NS:commctrl.tagNMMOUSE
title: tagNMMOUSE
author: windows-sdk-content
description: Contains information used with mouse notification messages.
old-location: controls\NMMOUSE.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\structures\nmmouse.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: "*LPNMMOUSE, LPNMMOUSE, LPNMMOUSE structure pointer [Windows Controls], NMCLICK, NMMOUSE, NMMOUSE structure [Windows Controls], _win32_NMMOUSE, _win32_NMMOUSE_cpp, commctrl/LPNMMOUSE, commctrl/NMMOUSE, controls.NMMOUSE, controls._win32_NMMOUSE, tagNMMOUSE"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NMMOUSE, *LPNMMOUSE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMMOUSE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMMOUSE structure


## -description


Contains information used with mouse notification messages. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about this notification. 


### -field dwItemSpec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD_PTR</a></b>

A control-specific item identifier. 


### -field dwItemData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD_PTR</a></b>

A control-specific item data. 


### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>


					A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that contains the client coordinates of the mouse when the click occurred. 


### -field dwHitInfo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Carries information about where on the item or control the cursor is pointing. 

