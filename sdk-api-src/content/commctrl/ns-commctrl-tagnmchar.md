---
UID: NS:commctrl.tagNMCHAR
title: tagNMCHAR
author: windows-sdk-content
description: Contains information used with character notification messages.
old-location: controls\NMCHAR.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmchar.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*LPNMCHAR, LPNMCHAR, LPNMCHAR structure pointer [Windows Controls], NMCHAR, NMCHAR structure [Windows Controls], _win32_NMCHAR, _win32_NMCHAR_cpp, commctrl/LPNMCHAR, commctrl/NMCHAR, controls.NMCHAR, controls._win32_NMCHAR, tagNMCHAR"
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
 - NMCHAR
product: Windows
targetos: Windows
req.typenames: NMCHAR, *LPNMCHAR
req.redist: 
---

# tagNMCHAR structure


## -description


Contains information used with character notification messages. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about this notification. 


### -field ch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The character that is being processed. 


### -field dwItemPrev

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A 32-bit value that is determined by the control that is sending the notification. 


### -field dwItemNext

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A 32-bit value that is determined by the control that is sending the notification. 

