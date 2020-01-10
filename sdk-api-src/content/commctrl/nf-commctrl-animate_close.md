---
UID: NF:commctrl.Animate_Close
title: Animate_Close macro (commctrl.h)
description: Closes an AVI clip. You can use this macro or send the ACM_OPEN message explicitly, passing in NULL parameters.
old-location: controls\Animate_Close.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\animation\macros\animate_close.htm
ms.date: 12/05/2018
ms.keywords: Animate_Close, Animate_Close macro [Windows Controls], _win32_Animate_Close, _win32_Animate_Close_cpp, commctrl/Animate_Close, controls.Animate_Close, controls._win32_Animate_Close
f1_keywords:
- commctrl/Animate_Close
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
- Animate_Close
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Animate_Close macro


## -description


Closes an AVI clip. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/acm-open">ACM_OPEN</a> message explicitly, passing in <b>NULL</b> parameters. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the animation control.


## -remarks



You can use <b>Animate_Close</b> to close an AVI file or AVI resource that was previously opened for the specified animation control.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-animate_open">Animate_Open</a>
 

 

