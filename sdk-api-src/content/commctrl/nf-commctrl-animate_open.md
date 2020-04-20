---
UID: NF:commctrl.Animate_Open
title: Animate_Open macro (commctrl.h)
description: Opens an AVI clip and displays its first frame in an animation control. You can use this macro or send the ACM_OPEN message explicitly.helpviewer_keywords: ["Animate_Open","Animate_Open macro [Windows Controls]","_win32_Animate_Open","_win32_Animate_Open_cpp","commctrl/Animate_Open","controls.Animate_Open","controls._win32_Animate_Open"]
old-location: controls\Animate_Open.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_open.htm
ms.date: 12/05/2018
ms.keywords: Animate_Open, Animate_Open macro [Windows Controls], _win32_Animate_Open, _win32_Animate_Open_cpp, commctrl/Animate_Open, controls.Animate_Open, controls._win32_Animate_Open
f1_keywords:
- commctrl/Animate_Open
dev_langs:
- c++
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
- Animate_Open
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Animate_Open macro


## -description


Opens an AVI clip and displays its first frame in an animation control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/acm-open">ACM_OPEN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the animation control. 


### -param szName

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource. Alternatively, this parameter can consist of the AVI resource identifier in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> and zero in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a>. To create this value, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. The control loads an AVI resource from the module specified by the instance handle passed to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> function, the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-animate_create">Animate_Create</a> macro, or the dialog box creation function that created the control. The AVI file or resource specified by <i>lpszName</i> must not contain audio.



If this parameter is <b>NULL</b>, the system closes the AVI file that was previously opened for the specified animation control, if any.


## -remarks



You can only open silent AVI clips. <a href="https://docs.microsoft.com/windows/desktop/Controls/acm-open">ACM_OPEN</a> and <b>Animate_Open</b> will fail if <i>lpszName</i> specifies an AVI clip that contains sound. 

You can use <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-animate_close">Animate_Close</a> to close an AVI file or AVI resource that was previously opened for the specified animation control. 



