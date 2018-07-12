---
UID: NF:windowsx.Static_SetIcon
title: Static_SetIcon macro
author: windows-sdk-content
description: Sets the icon for a static control. You can use this macro or send the STM_SETICON message explicitly.
old-location: controls\Static_SetIcon.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_seticon.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: Static_SetIcon, Static_SetIcon macro [Windows Controls], _win32_Static_SetIcon, _win32_Static_SetIcon_cpp, controls.Static_SetIcon, controls._win32_Static_SetIcon, windowsx/Static_SetIcon
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - Static_SetIcon
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Static_SetIcon macro


## -description


Sets the icon for a static control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb760780(v=VS.85).aspx">STM_SETICON</a> message explicitly. 



## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param hIcon

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HICON</a></b>

a handle to the icon.

