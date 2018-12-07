---
UID: NF:commctrl.Animate_Play
title: Animate_Play macro
author: windows-sdk-content
description: Plays an AVI clip in an animation control. The control plays the clip in the background while the thread continues executing. You can use this macro or send the ACM_PLAY message explicitly.
old-location: controls\Animate_Play.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_play.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Animate_Play, Animate_Play macro [Windows Controls], _win32_Animate_Play, _win32_Animate_Play_cpp, commctrl/Animate_Play, controls.Animate_Play, controls._win32_Animate_Play
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
 - Animate_Play
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Animate_Play macro


## -description


Plays an AVI clip in an animation control. The control plays the clip in the background while the thread continues executing. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761899(v=VS.85).aspx">ACM_PLAY</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the animation control in which to play the AVI clip. 


### -param from

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The zero-based index of the frame where playing begins. The value must be less than 65,536. A value of zero means begin with the first frame in the AVI clip. 


### -param to

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The zero-based index of the frame where playing ends. The value must be less than 65,536. A value of -1 means end with the last frame in the AVI clip. 


### -param rep

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of times to replay the AVI clip. A value of -1 means replay the clip indefinitely.


## -remarks



You can use <a href="https://msdn.microsoft.com/en-us/library/Bb761916(v=VS.85).aspx">Animate_Seek</a> to direct the animation control to display a particular frame of the AVI clip. 



