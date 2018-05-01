---
UID: NS:richedit._endropfiles
title: "_endropfiles"
author: windows-driver-content
description: Contains information associated with an EN_DROPFILES notification code. A rich edit control sends this notification code when it receives a WM_DROPFILES message.
old-location: controls\ENDROPFILES.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\endropfiles.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ENDROPFILES, ENDROPFILES structure [Windows Controls], _endropfiles, _win32_ENDROPFILES_str, _win32_ENDROPFILES_str_cpp, controls.ENDROPFILES, controls._win32_ENDROPFILES_str, richedit/ENDROPFILES
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
req.typenames: ENDROPFILES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Richedit.h
api_name:
-	ENDROPFILES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _endropfiles structure


## -description



			Contains information associated with an <a href="https://msdn.microsoft.com/fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3">EN_DROPFILES</a> notification code. A rich edit control sends this notification code when it receives a <a href="https://msdn.microsoft.com/07dc2df7-4699-4e9c-b1a5-4ce877116268">WM_DROPFILES</a> message.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


            Notification header. 


### -field hDrop

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a></b>

Handle to the dropped files list (same as with <a href="https://msdn.microsoft.com/07dc2df7-4699-4e9c-b1a5-4ce877116268">WM_DROPFILES</a> ). This handle is used with the <a href="https://msdn.microsoft.com/9b15e8a5-de68-4dcb-8e1a-0ee0393aa9db">DragFinish</a>, <a href="https://msdn.microsoft.com/93fab381-9035-46c4-ba9d-efb2d0801d84">DragQueryFile</a>, and <a href="https://msdn.microsoft.com/87794ab0-a075-4a1f-869f-5998bdc57a1d">DragQueryPoint</a> functions. 


### -field cp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Character position at which the dropped files would be inserted. 


### -field fProtected

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>


            Indicates whether the specified character position is protected (<b>TRUE</b>) or not protected (<b>FALSE</b>).

