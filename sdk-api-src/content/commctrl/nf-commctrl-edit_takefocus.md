---
UID: NF:commctrl.Edit_TakeFocus
title: Edit_TakeFocus macro (commctrl.h)
description: Forces a single-line edit control to receive keyboard focus. You can use this macro or send the EM_TAKEFOCUS message explicitly.
helpviewer_keywords: ["Edit_TakeFocus","Edit_TakeFocus macro [Windows Controls]","_win32_Edit_TakeFocus","_win32_Edit_TakeFocus_cpp","commctrl/Edit_TakeFocus","controls.Edit_TakeFocus","controls._win32_Edit_TakeFocus"]
old-location: controls\Edit_TakeFocus.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_takefocus.htm
ms.date: 12/05/2018
ms.keywords: Edit_TakeFocus, Edit_TakeFocus macro [Windows Controls], _win32_Edit_TakeFocus, _win32_Edit_TakeFocus_cpp, commctrl/Edit_TakeFocus, controls.Edit_TakeFocus, controls._win32_Edit_TakeFocus
f1_keywords:
- commctrl/Edit_TakeFocus
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Edit_TakeFocus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_TakeFocus macro


## -description


<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Forces a single-line edit control to receive keyboard focus. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-takefocus">EM_TAKEFOCUS</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the edit control.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/Controls/em-takefocus">EM_TAKEFOCUS</a> message is ignored if the edit control is not a single-line edit control.

If the edit control previously received an <a href="https://docs.microsoft.com/windows/desktop/Controls/em-nosetfocus">EM_NOSETFOCUS</a> message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/em-nosetfocus">EM_NOSETFOCUS</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/em-takefocus">EM_TAKEFOCUS</a>



<b>Reference</b>
 

 

