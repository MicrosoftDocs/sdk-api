---
UID: NS:commctrl.tagLVKEYDOWN
title: tagLVKEYDOWN
author: windows-sdk-content
description: Contains information used in processing the LVN_KEYDOWN notification code. This structure is the same as the NMLVKEYDOWN structure but has been renamed to fit standard naming conventions.
old-location: controls\NMLVKEYDOWN.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvkeydown.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: "*LPNMLVKEYDOWN, LPNMLVKEYDOWN, LPNMLVKEYDOWN structure pointer [Windows Controls], NMLVKEYDOWN, NMLVKEYDOWN structure [Windows Controls], _win32_NMLVKEYDOWN, _win32_NMLVKEYDOWN_cpp, commctrl/LPNMLVKEYDOWN, commctrl/NMLVKEYDOWN, controls.NMLVKEYDOWN, controls._win32_NMLVKEYDOWN, tagLVKEYDOWN"
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
req.typenames: NMLVKEYDOWN, *LPNMLVKEYDOWN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMLVKEYDOWN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagLVKEYDOWN structure


## -description


Contains information used in processing the <a href="https://msdn.microsoft.com/library/Bb774849(v=VS.85).aspx">LVN_KEYDOWN</a> notification code. This structure is the same as the 
			<b>NMLVKEYDOWN</b> structure but has been renamed to fit standard naming conventions. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field wVKey

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>


<a href="https://msdn.microsoft.com/library/Dd375731(v=VS.85).aspx">Virtual key code</a>. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

This member must always be zero. 

