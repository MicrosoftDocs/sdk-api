---
UID: NF:commctrl.Header_GetOverflowRect
title: Header_GetOverflowRect macro
author: windows-sdk-content
description: Gets the coordinates of the drop-down overflow area for a specified header control. The header control must be of type HDF_SPLITBUTTON. Use this macro or send the HDM_GETOVERFLOWRECT message explicitly.
old-location: controls\Header_GetOverflowRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getoverflowrect.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: Header_GetOverflowRect, Header_GetOverflowRect macro [Windows Controls], _shell_Header_GetOverflowRect, _shell_Header_GetOverflowRect_cpp, commctrl/Header_GetOverflowRect, controls.Header_GetOverflowRect, controls._shell_Header_GetOverflowRect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	Header_GetOverflowRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Header_GetOverflowRect macro


## -description


Gets the coordinates of the drop-down overflow area for a specified header control. The header control must be of type <b>HDF_SPLITBUTTON</b>. Use this macro or send the <a href="https://msdn.microsoft.com/52fb3dc3-ce22-40da-8222-20fd75c005ae">HDM_GETOVERFLOWRECT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control.


### -param lprc

TBD






#### - lpItemRect [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure to receive the bounding rectangle information.The message sender is responsible for allocating this structure. The coordinates returned in the <b>RECT</b> structure are expressed as screen coordinates.

