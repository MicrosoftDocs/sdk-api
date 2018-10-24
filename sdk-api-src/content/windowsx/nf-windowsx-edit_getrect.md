---
UID: NF:windowsx.Edit_GetRect
title: Edit_GetRect macro
author: windows-sdk-content
description: Gets the formatting rectangle of an edit control. You can use this macro or send the EM_GETRECT message explicitly.
old-location: controls\Edit_GetRect.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getrect.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: Edit_GetRect, Edit_GetRect macro [Windows Controls], _win32_Edit_GetRect, _win32_Edit_GetRect_cpp, controls.Edit_GetRect, controls._win32_Edit_GetRect, windowsx/Edit_GetRect
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
 - Edit_GetRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_GetRect macro


## -description


Gets the formatting rectangle of an edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/eef0150d-9b7a-4247-acbf-6fea2efd1dc3">EM_GETRECT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lprc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the formatting rectangle. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/eef0150d-9b7a-4247-acbf-6fea2efd1dc3">EM_GETRECT</a>.



