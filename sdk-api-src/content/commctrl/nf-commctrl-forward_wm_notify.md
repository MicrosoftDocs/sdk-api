---
UID: NF:commctrl.FORWARD_WM_NOTIFY
title: FORWARD_WM_NOTIFY macro
author: windows-driver-content
description: Sends or posts the WM_NOTIFY message.
old-location: controls\FORWARD_WM_NOTIFY.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\macros\forward_wm_notify.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: FORWARD_WM_NOTIFY, FORWARD_WM_NOTIFY macro [Windows Controls], _win32_FORWARD_WM_NOTIFY, _win32_FORWARD_WM_NOTIFY_cpp, commctrl/FORWARD_WM_NOTIFY, controls.FORWARD_WM_NOTIFY, controls._win32_FORWARD_WM_NOTIFY
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
-	FORWARD_WM_NOTIFY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# FORWARD_WM_NOTIFY macro


## -description


Sends or posts the <a href="https://msdn.microsoft.com/23ff9dc1-3d92-4e94-8df5-7a645039ce27">WM_NOTIFY</a> message. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that receives the <a href="https://msdn.microsoft.com/23ff9dc1-3d92-4e94-8df5-7a645039ce27">WM_NOTIFY</a> message. 


### -param idFrom

Type: <b>int</b>

The identifier of the control sending the message. 


### -param pnmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains the notification code and additional information. For some notification codes, this parameter points to a larger structure that has the <b>NMHDR</b> structure as its first member. 


### -param fn

Type: <b>function</b>

The function that sends or posts the <a href="https://msdn.microsoft.com/23ff9dc1-3d92-4e94-8df5-7a645039ce27">WM_NOTIFY</a> message. This parameter can be either the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a> or <a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a> function. 


## -remarks



The <b>FORWARD_WM_NOTIFY</b> macro is defined as follows. 

<pre class="syntax" xml:space="preserve"><code>#define FORWARD_WM_NOTIFY(hwnd, idFrom, pnmhdr, fn) \ 

    (void)(fn)((hwnd), WM_NOTIFY, (WPARAM)(int)(id), \ 
    (LPARAM)(NMHDR*)(pnmhdr)) </code></pre>


