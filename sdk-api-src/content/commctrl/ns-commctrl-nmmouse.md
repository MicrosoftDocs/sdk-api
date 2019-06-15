---
UID: NS:commctrl.tagNMMOUSE
title: NMMOUSE (commctrl.h)
author: windows-sdk-content
description: Contains information used with mouse notification messages.
old-location: controls\NMMOUSE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmmouse.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPNMMOUSE, LPNMMOUSE, LPNMMOUSE structure pointer [Windows Controls], NMCLICK, NMMOUSE, NMMOUSE structure [Windows Controls], _win32_NMMOUSE, _win32_NMMOUSE_cpp, commctrl/LPNMMOUSE, commctrl/NMMOUSE, controls.NMMOUSE, controls._win32_NMMOUSE"
ms.topic: struct
f1_keywords: ["commctrl/NMMOUSE"]
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
 - NMMOUSE
product: Windows
targetos: Windows
req.typenames: NMMOUSE, *LPNMMOUSE
req.redist: 
ms.custom: 19H1
---

# NMMOUSE structure


## -description


Contains information used with mouse notification messages. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-_nmhdr">NMHDR</a></b>

An <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-_nmhdr">NMHDR</a> structure that contains additional information about this notification. 


### -field dwItemSpec

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

A control-specific item identifier. 


### -field dwItemData

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

A control-specific item data. 


### -field pt

Type: <b><a href="https://docs.microsoft.com/previous-versions//dd162805(v=vs.85)">POINT</a></b>

A <a href="https://docs.microsoft.com/previous-versions//dd162805(v=vs.85)">POINT</a> structure that contains the client coordinates of the mouse when the click occurred. 


### -field dwHitInfo

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Carries information about where on the item or control the cursor is pointing. 

