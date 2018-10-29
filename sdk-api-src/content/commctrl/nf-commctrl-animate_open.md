---
UID: NF:commctrl.Animate_Open
title: Animate_Open macro
author: windows-sdk-content
description: Opens an AVI clip and displays its first frame in an animation control. You can use this macro or send the ACM_OPEN message explicitly.
old-location: controls\Animate_Open.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_open.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: Animate_Open, Animate_Open macro [Windows Controls], _win32_Animate_Open, _win32_Animate_Open_cpp, commctrl/Animate_Open, controls.Animate_Open, controls._win32_Animate_Open
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
 - Animate_Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Animate_Open macro


## -description


Opens an AVI clip and displays its first frame in an animation control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761897(v=VS.85).aspx">ACM_OPEN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the animation control. 


### -param szName

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPTSTR</a></b>

A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource. Alternatively, this parameter can consist of the AVI resource identifier in the <a href="https://msdn.microsoft.com/en-us/library/ms632659(v=VS.85).aspx">LOWORD</a> and zero in the <a href="https://msdn.microsoft.com/en-us/library/ms632657(v=VS.85).aspx">HIWORD</a>. To create this value, use the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro. The control loads an AVI resource from the module specified by the instance handle passed to the <a href="https://msdn.microsoft.com/en-us/library/ms632679(v=VS.85).aspx">CreateWindow</a> function, the <a href="https://msdn.microsoft.com/en-us/library/Bb761904(v=VS.85).aspx">Animate_Create</a> macro, or the dialog box creation function that created the control. The AVI file or resource specified by <i>lpszName</i> must not contain audio.



If this parameter is <b>NULL</b>, the system closes the AVI file that was previously opened for the specified animation control, if any.


## -remarks



You can only open silent AVI clips. <a href="https://msdn.microsoft.com/en-us/library/Bb761897(v=VS.85).aspx">ACM_OPEN</a> and <b>Animate_Open</b> will fail if <i>lpszName</i> specifies an AVI clip that contains sound. 

You can use <a href="https://msdn.microsoft.com/en-us/library/Bb761902(v=VS.85).aspx">Animate_Close</a> to close an AVI file or AVI resource that was previously opened for the specified animation control. 



