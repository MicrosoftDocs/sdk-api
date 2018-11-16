---
UID: NS:commctrl.tagNMMOUSE
title: tagNMMOUSE
author: windows-sdk-content
description: Contains information used with mouse notification messages.
old-location: controls\NMMOUSE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmmouse.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPNMMOUSE, LPNMMOUSE, LPNMMOUSE structure pointer [Windows Controls], NMCLICK, NMMOUSE, NMMOUSE structure [Windows Controls], _win32_NMMOUSE, _win32_NMMOUSE_cpp, commctrl/LPNMMOUSE, commctrl/NMMOUSE, controls.NMMOUSE, controls._win32_NMMOUSE, tagNMMOUSE"
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
 - NMMOUSE
product: Windows
targetos: Windows
req.typenames: NMMOUSE, *LPNMMOUSE
req.redist: 
---

# tagNMMOUSE structure


## -description


Contains information used with mouse notification messages. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about this notification. 


### -field dwItemSpec

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD_PTR</a></b>

A control-specific item identifier. 


### -field dwItemData

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD_PTR</a></b>

A control-specific item data. 


### -field pt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

A <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the client coordinates of the mouse when the click occurred. 


### -field dwHitInfo

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPARAM</a></b>

Carries information about where on the item or control the cursor is pointing. 

