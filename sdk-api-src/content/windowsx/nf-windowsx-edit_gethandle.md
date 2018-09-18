---
UID: NF:windowsx.Edit_GetHandle
title: Edit_GetHandle macro
author: windows-sdk-content
description: Gets a handle to the memory currently allocated for the text of a multiline edit control. You can use this macro or send the EM_GETHANDLE message explicitly.
old-location: controls\Edit_GetHandle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_gethandle.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Edit_GetHandle, Edit_GetHandle macro [Windows Controls], _win32_Edit_GetHandle, _win32_Edit_GetHandle_cpp, controls.Edit_GetHandle, controls._win32_Edit_GetHandle, windowsx/Edit_GetHandle
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
 - Edit_GetHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_GetHandle macro


## -description


Gets a handle to the memory currently allocated for the text of a multiline edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/74271812-9715-4a46-96b3-0788134f8143">EM_GETHANDLE</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/74271812-9715-4a46-96b3-0788134f8143">EM_GETHANDLE</a>.



