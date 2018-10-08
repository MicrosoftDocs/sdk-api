---
UID: NF:windowsx.Edit_CanUndo
title: Edit_CanUndo macro
author: windows-sdk-content
description: Determines whether there are any actions in the undo queue of an edit or rich edit control. You can use this macro or send the EM_CANUNDO message explicitly.
old-location: controls\Edit_CanUndo.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_canundo.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: Edit_CanUndo, Edit_CanUndo macro [Windows Controls], _win32_Edit_CanUndo, _win32_Edit_CanUndo_cpp, controls.Edit_CanUndo, controls._win32_Edit_CanUndo, windowsx/Edit_CanUndo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: windowsx.h
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
 - Windowsx.h
api_name:
 - Edit_CanUndo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_CanUndo macro


## -description


Determines whether there are any actions in the undo queue of an edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775468(v=VS.85).aspx">EM_CANUNDO</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775468(v=VS.85).aspx">EM_CANUNDO</a>.



