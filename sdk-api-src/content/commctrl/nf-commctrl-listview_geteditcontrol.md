---
UID: NF:commctrl.ListView_GetEditControl
title: ListView_GetEditControl macro
author: windows-driver-content
description: Gets the handle to the edit control being used to edit a list-view item's text. You can use this macro or send the LVM_GETEDITCONTROL message explicitly.
old-location: controls\ListView_GetEditControl.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_geteditcontrol.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ListView_GetEditControl, ListView_GetEditControl macro [Windows Controls], _win32_ListView_GetEditControl, _win32_ListView_GetEditControl_cpp, commctrl/ListView_GetEditControl, controls.ListView_GetEditControl, controls._win32_ListView_GetEditControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_GetEditControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetEditControl macro


## -description


Gets the handle to the edit control being used to edit a list-view item's text. You can use this macro or send the <a href="https://msdn.microsoft.com/70450b24-9879-4be8-9bc9-f87008b66415">LVM_GETEDITCONTROL</a> message explicitly. 


## -parameters




### -param hwndLV

TBD






#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



When label editing begins, an edit control is created, positioned, and initialized. Before it is displayed, the list-view control sends its parent window an <a href="https://msdn.microsoft.com/c13a9e95-22a9-476e-aeee-4928b8b096b0">LVN_BEGINLABELEDIT</a> notification code. 

To customize label editing, implement a handler for <a href="https://msdn.microsoft.com/c13a9e95-22a9-476e-aeee-4928b8b096b0">LVN_BEGINLABELEDIT</a> and have it use <b>ListView_GetEditControl</b> to send an <a href="https://msdn.microsoft.com/70450b24-9879-4be8-9bc9-f87008b66415">LVM_GETEDITCONTROL</a> message to the list-view control. If a label is being edited, the return value will be a handle to the edit control. Use this handle to customize the edit control by sending the usual 
				<b>EM_XXX</b> messages. 

When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid. You can subclass the edit control, but you should not destroy it. To cancel editing, you can send the list-view control a <a href="https://msdn.microsoft.com/c801233a-c4d8-4fd9-aaf0-3d4503bbce26">WM_CANCELMODE</a> message.

The list-view item being edited is the currently focused item—that is, the item in the focused state. To find an item based on its state, use the <a href="https://msdn.microsoft.com/2d458f12-b9d3-4b9e-bcb4-927c14c16537">LVM_GETNEXTITEM</a> message.




## -see-also




<a href="https://msdn.microsoft.com/70450b24-9879-4be8-9bc9-f87008b66415">LVM_GETEDITCONTROL</a>
 

 

