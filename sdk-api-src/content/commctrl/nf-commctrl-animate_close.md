---
UID: NF:commctrl.Animate_Close
title: Animate_Close macro
author: windows-sdk-content
description: Closes an AVI clip. You can use this macro or send the ACM_OPEN message explicitly, passing in NULL parameters.
old-location: controls\Animate_Close.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_close.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Animate_Close, Animate_Close macro [Windows Controls], _win32_Animate_Close, _win32_Animate_Close_cpp, commctrl/Animate_Close, controls.Animate_Close, controls._win32_Animate_Close
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
 - Animate_Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Animate_Close macro


## -description


Closes an AVI clip. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761897(v=VS.85).aspx">ACM_OPEN</a> message explicitly, passing in <b>NULL</b> parameters. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the animation control.


## -remarks



You can use <b>Animate_Close</b> to close an AVI file or AVI resource that was previously opened for the specified animation control.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb761908(v=VS.85).aspx">Animate_Open</a>
 

 

