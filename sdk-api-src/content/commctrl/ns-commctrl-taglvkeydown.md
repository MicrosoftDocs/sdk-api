---
UID: NS:commctrl.tagLVKEYDOWN
title: tagLVKEYDOWN
author: windows-driver-content
description: Contains information used in processing the LVN_KEYDOWN notification code. This structure is the same as the NMLVKEYDOWN structure but has been renamed to fit standard naming conventions.
old-location: controls\NMLVKEYDOWN.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvkeydown.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: "*LPNMLVKEYDOWN, LPNMLVKEYDOWN, LPNMLVKEYDOWN structure pointer [Windows Controls], NMLVKEYDOWN, NMLVKEYDOWN structure [Windows Controls], _win32_NMLVKEYDOWN, _win32_NMLVKEYDOWN_cpp, commctrl/LPNMLVKEYDOWN, commctrl/NMLVKEYDOWN, controls.NMLVKEYDOWN, controls._win32_NMLVKEYDOWN, tagLVKEYDOWN"
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
req.typenames: NMLVKEYDOWN, *LPNMLVKEYDOWN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMLVKEYDOWN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagLVKEYDOWN structure


## -description


Contains information used in processing the <a href="https://msdn.microsoft.com/3aa3d165-7227-41c4-8bc2-3e51a0f52ee3">LVN_KEYDOWN</a> notification code. This structure is the same as the 
			<b>NMLVKEYDOWN</b> structure but has been renamed to fit standard naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field wVKey

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>


<a href="https://msdn.microsoft.com/fa8926ad-41b2-4164-9ba3-ae501fd0eef2">Virtual key code</a>. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

This member must always be zero. 

