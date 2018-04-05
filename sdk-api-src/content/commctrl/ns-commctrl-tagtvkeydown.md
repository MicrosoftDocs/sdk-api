---
UID: NS:commctrl.tagTVKEYDOWN
title: tagTVKEYDOWN
author: windows-driver-content
description: Contains information about a keyboard event in a tree-view control. This structure is used with the TVN_KEYDOWN notification code. The structure is identical to the TV_KEYDOWN structure, but it has been renamed to follow current naming conventions.
old-location: controls\NMTVKEYDOWN.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvkeydown.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: "*LPNMTVKEYDOWN, LPNMTVKEYDOWN, LPNMTVKEYDOWN structure pointer [Windows Controls], NMTVKEYDOWN, NMTVKEYDOWN structure [Windows Controls], _win32_NMTVKEYDOWN, _win32_NMTVKEYDOWN_cpp, commctrl/LPNMTVKEYDOWN, commctrl/NMTVKEYDOWN, controls.NMTVKEYDOWN, controls._win32_NMTVKEYDOWN, tagTVKEYDOWN"
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
req.typenames: NMTVKEYDOWN, *LPNMTVKEYDOWN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMTVKEYDOWN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagTVKEYDOWN structure


## -description


Contains information about a keyboard event in a tree-view control. This structure is used with the <a href="https://msdn.microsoft.com/da0d2b62-2295-4dce-9b37-a250f3be087f">TVN_KEYDOWN</a> notification code. The structure is identical to the 
			<b>TV_KEYDOWN</b> structure, but it has been renamed to follow current naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification. 


### -field wVKey

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Virtual key code. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Always zero. 


## -see-also




<a href="https://msdn.microsoft.com/23ff9dc1-3d92-4e94-8df5-7a645039ce27">WM_NOTIFY</a>
 

 

