---
UID: NF:commctrl.ListView_GetEditControl
title: ListView_GetEditControl macro
author: windows-sdk-content
description: Gets the handle to the edit control being used to edit a list-view item's text. You can use this macro or send the LVM_GETEDITCONTROL message explicitly.
old-location: controls\ListView_GetEditControl.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_geteditcontrol.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
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
 - ListView_GetEditControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetEditControl macro


## -description


Gets the handle to the edit control being used to edit a list-view item's text. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774919(v=VS.85).aspx">LVM_GETEDITCONTROL</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


## -remarks



When label editing begins, an edit control is created, positioned, and initialized. Before it is displayed, the list-view control sends its parent window an <a href="https://msdn.microsoft.com/en-us/library/Bb774798(v=VS.85).aspx">LVN_BEGINLABELEDIT</a> notification code. 

To customize label editing, implement a handler for <a href="https://msdn.microsoft.com/en-us/library/Bb774798(v=VS.85).aspx">LVN_BEGINLABELEDIT</a> and have it use <b>ListView_GetEditControl</b> to send an <a href="https://msdn.microsoft.com/en-us/library/Bb774919(v=VS.85).aspx">LVM_GETEDITCONTROL</a> message to the list-view control. If a label is being edited, the return value will be a handle to the edit control. Use this handle to customize the edit control by sending the usual 
				<b>EM_XXX</b> messages. 

When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid. You can subclass the edit control, but you should not destroy it. To cancel editing, you can send the list-view control a <a href="https://msdn.microsoft.com/en-us/library/ms632615(v=VS.85).aspx">WM_CANCELMODE</a> message.

The list-view item being edited is the currently focused item—that is, the item in the focused state. To find an item based on its state, use the <a href="https://msdn.microsoft.com/en-us/library/Bb761057(v=VS.85).aspx">LVM_GETNEXTITEM</a> message.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774919(v=VS.85).aspx">LVM_GETEDITCONTROL</a>
 

 

