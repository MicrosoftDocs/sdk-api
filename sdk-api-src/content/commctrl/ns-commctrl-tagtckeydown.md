---
UID: NS:commctrl.tagTCKEYDOWN
title: tagTCKEYDOWN
author: windows-sdk-content
description: Contains information about a key press in a tab control. It is used with the TCN_KEYDOWN notification code. This structure supersedes the TC_KEYDOWN structure.
old-location: controls\NMTCKEYDOWN.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\tab\structures\nmtckeydown.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: NMTCKEYDOWN, NMTCKEYDOWN structure [Windows Controls], _win32_NMTCKEYDOWN, _win32_NMTCKEYDOWN_cpp, commctrl/NMTCKEYDOWN, controls.NMTCKEYDOWN, controls._win32_NMTCKEYDOWN, tagTCKEYDOWN
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
req.typenames: NMTCKEYDOWN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMTCKEYDOWN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagTCKEYDOWN structure


## -description


Contains information about a key press in a tab control. It is used with the <a href="https://msdn.microsoft.com/library/Bb760567(v=VS.85).aspx">TCN_KEYDOWN</a> notification code. This structure supersedes the
<b>TC_KEYDOWN</b> structure. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about the notification. 


### -field wVKey

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Virtual key code. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Value that is identical to the 
					<i>lParam</i> parameter of the <a href="https://msdn.microsoft.com/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> message. 

