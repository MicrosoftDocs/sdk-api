---
UID: NF:windowsx.Edit_GetFirstVisibleLine
title: Edit_GetFirstVisibleLine macro
author: windows-driver-content
description: Gets the index of the uppermost visible line in a multiline edit or rich edit control. You can use this macro or send the EM_GETFIRSTVISIBLELINE message explicitly.
old-location: controls\Edit_GetFirstVisibleLine.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getfirstvisibleline.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: Edit_GetFirstVisibleLine, Edit_GetFirstVisibleLine macro [Windows Controls], _win32_Edit_GetFirstVisibleLine, _win32_Edit_GetFirstVisibleLine_cpp, controls.Edit_GetFirstVisibleLine, controls._win32_Edit_GetFirstVisibleLine, windowsx/Edit_GetFirstVisibleLine
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
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windowsx.h
api_name:
-	Edit_GetFirstVisibleLine
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_GetFirstVisibleLine macro


## -description


Gets the index of the uppermost visible line in a multiline edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/022838d2-7948-4c5a-92ca-655822c4f672">EM_GETFIRSTVISIBLELINE</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/022838d2-7948-4c5a-92ca-655822c4f672">EM_GETFIRSTVISIBLELINE</a>.



