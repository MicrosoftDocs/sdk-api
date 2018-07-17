---
UID: NF:commctrl.Animate_Seek
title: Animate_Seek macro
author: windows-sdk-content
description: Directs an animation control to display a particular frame of an AVI clip. The control displays the clip in the background while the thread continues executing. You can use this macro or send the ACM_PLAY message explicitly.
old-location: controls\Animate_Seek.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_seek.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Animate_Seek, Animate_Seek macro [Windows Controls], _win32_Animate_Seek, _win32_Animate_Seek_cpp, commctrl/Animate_Seek, controls.Animate_Seek, controls._win32_Animate_Seek
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Animate_Seek
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Animate_Seek macro


## -description


Directs an animation control to display a particular frame of an AVI clip. The control displays the clip in the background while the thread continues executing. You can use this macro or send the <a href="https://msdn.microsoft.com/738b7305-bb77-441d-a198-17daf3b76039">ACM_PLAY</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param frame

TBD






#### - hwndAnim

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the animation control in which to display the AVI frame. 


#### - wFrame

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based index of the frame to display. 


## -see-also




<a href="https://msdn.microsoft.com/41865bd5-2729-423c-866b-e4afafa19b3a">Animate_Play</a>
 

 

