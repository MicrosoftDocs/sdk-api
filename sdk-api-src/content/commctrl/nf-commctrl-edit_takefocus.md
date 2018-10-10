---
UID: NF:commctrl.Edit_TakeFocus
title: Edit_TakeFocus macro
author: windows-sdk-content
description: Forces a single-line edit control to receive keyboard focus. You can use this macro or send the EM_TAKEFOCUS message explicitly.
old-location: controls\Edit_TakeFocus.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_takefocus.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Edit_TakeFocus, Edit_TakeFocus macro [Windows Controls], _win32_Edit_TakeFocus, _win32_Edit_TakeFocus_cpp, commctrl/Edit_TakeFocus, controls.Edit_TakeFocus, controls._win32_Edit_TakeFocus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_TakeFocus macro


## -description


<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Forces a single-line edit control to receive keyboard focus. You can use this macro or send the <a href="https://msdn.microsoft.com/27470857-4219-4426-bc69-e1271afc6ffb">EM_TAKEFOCUS</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the edit control.


## -remarks



The <a href="https://msdn.microsoft.com/27470857-4219-4426-bc69-e1271afc6ffb">EM_TAKEFOCUS</a> message is ignored if the edit control is not a single-line edit control.

If the edit control previously received an <a href="https://msdn.microsoft.com/aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c">EM_NOSETFOCUS</a> message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.




## -see-also




<a href="https://msdn.microsoft.com/aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c">EM_NOSETFOCUS</a>



<a href="https://msdn.microsoft.com/27470857-4219-4426-bc69-e1271afc6ffb">EM_TAKEFOCUS</a>



<b>Reference</b>
 

 

