---
UID: NF:commctrl.Animate_OpenEx
title: Animate_OpenEx macro
author: windows-sdk-content
description: Opens an AVI clip from a resource in a specified module and displays its first frame in an animation control. You can use this macro or send the ACM_OPEN message explicitly.
old-location: controls\Animate_OpenEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_openex.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Animate_OpenEx, Animate_OpenEx macro [Windows Controls], _win32_Animate_OpenEx, _win32_Animate_OpenEx_cpp, commctrl/Animate_OpenEx, controls.Animate_OpenEx, controls._win32_Animate_OpenEx
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
 - Animate_OpenEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Animate_OpenEx macro


## -description


Opens an AVI clip from a resource in a specified module and displays its first frame in an animation control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761897(v=VS.85).aspx">ACM_OPEN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the animation control. 


### -param hInst

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HINSTANCE</a></b>

An instance handle to the module from which the resource should be loaded. If this value is <b>NULL</b>, the resource is loaded from the module that created the animation control. 


### -param szName

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPTSTR</a></b>

A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource. Alternatively, this parameter can consist of the AVI resource identifier in the <a href="https://msdn.microsoft.com/en-us/library/ms632659(v=VS.85).aspx">LOWORD</a> and zero in the <a href="https://msdn.microsoft.com/en-us/library/ms632657(v=VS.85).aspx">HIWORD</a>. To create this value, use the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro. The control loads the AVI resource from the module specified by <i>hinst</i>. The AVI file or resource specified by <i>lpszName</i> must not contain audio.



If this parameter is <b>NULL</b>, the system closes the AVI file that was previously opened for the specified animation control, if any.


## -remarks



You can only open silent AVI clips. <a href="https://msdn.microsoft.com/en-us/library/Bb761897(v=VS.85).aspx">ACM_OPEN</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb761908(v=VS.85).aspx">Animate_Open</a> will fail if <i>lpszName</i> specifies an AVI clip that contains sound. 

You can use <a href="https://msdn.microsoft.com/en-us/library/Bb761902(v=VS.85).aspx">Animate_Close</a> to close an AVI file or AVI resource that was previously opened for the specified animation control. 



