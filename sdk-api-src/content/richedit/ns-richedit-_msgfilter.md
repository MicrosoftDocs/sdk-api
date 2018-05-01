---
UID: NS:richedit._msgfilter
title: "_msgfilter"
author: windows-driver-content
description: Contains information about a keyboard or mouse event. A rich edit control sends this structure to its parent window as part of an EN_MSGFILTER notification code, enabling the parent to change the message or prevent it from being processed.
old-location: controls\MSGFILTER.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\msgfilter.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: MSGFILTER, MSGFILTER structure [Windows Controls], _msgfilter, _win32_MSGFILTER_str, _win32_MSGFILTER_str_cpp, controls.MSGFILTER, controls._win32_MSGFILTER_str, richedit/MSGFILTER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MSGFILTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Richedit.h
api_name:
-	MSGFILTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _msgfilter structure


## -description


Contains information about a keyboard or mouse event. A rich edit control sends this structure to its parent window as part of an <a href="https://msdn.microsoft.com/96cf0047-baae-46cd-82e8-ab6f3f353260">EN_MSGFILTER</a> notification code, enabling the parent to change the message or prevent it from being processed.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

The <b>code</b> member of the <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure is the <a href="https://msdn.microsoft.com/96cf0047-baae-46cd-82e8-ab6f3f353260">EN_MSGFILTER</a> notification code that identifies the message being sent. 


### -field msg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Keyboard or mouse message identifier. 


### -field wParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

The 
					<b>wParam</b> parameter of the message. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The 
					<b>lParam</b> parameter of the message. 


## -see-also




<a href="https://msdn.microsoft.com/96cf0047-baae-46cd-82e8-ab6f3f353260">EN_MSGFILTER</a>
 

 

