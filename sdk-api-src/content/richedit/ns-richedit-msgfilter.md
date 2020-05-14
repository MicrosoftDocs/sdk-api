---
UID: NS:richedit._msgfilter
title: MSGFILTER (richedit.h)
description: Contains information about a keyboard or mouse event. A rich edit control sends this structure to its parent window as part of an EN_MSGFILTER notification code, enabling the parent to change the message or prevent it from being processed.helpviewer_keywords: ["MSGFILTER","MSGFILTER structure [Windows Controls]","_win32_MSGFILTER_str","_win32_MSGFILTER_str_cpp","controls.MSGFILTER","controls._win32_MSGFILTER_str","richedit/MSGFILTER"]
old-location: controls\MSGFILTER.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\msgfilter.htm
ms.date: 12/05/2018
ms.keywords: MSGFILTER, MSGFILTER structure [Windows Controls], _win32_MSGFILTER_str, _win32_MSGFILTER_str_cpp, controls.MSGFILTER, controls._win32_MSGFILTER_str, richedit/MSGFILTER
f1_keywords:
- richedit/MSGFILTER
dev_langs:
- c++
req.header: richedit.h
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
- Richedit.h
api_name:
- MSGFILTER
targetos: Windows
req.typenames: MSGFILTER
req.redist: 
ms.custom: 19H1
---

# MSGFILTER structure


## -description


Contains information about a keyboard or mouse event. A rich edit control sends this structure to its parent window as part of an <a href="https://msdn.microsoft.com/96cf0047-baae-46cd-82e8-ab6f3f353260">EN_MSGFILTER</a> notification code, enabling the parent to change the message or prevent it from being processed.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

The <b>code</b> member of the <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure is the <a href="https://msdn.microsoft.com/96cf0047-baae-46cd-82e8-ab6f3f353260">EN_MSGFILTER</a> notification code that identifies the message being sent. 


### -field msg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Keyboard or mouse message identifier. 


### -field wParam

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

The 
					<b>wParam</b> parameter of the message. 


### -field lParam

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The 
					<b>lParam</b> parameter of the message. 


## -see-also




<a href="https://msdn.microsoft.com/96cf0047-baae-46cd-82e8-ab6f3f353260">EN_MSGFILTER</a>
 

 

