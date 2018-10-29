---
UID: NF:windowsx.ScrollBar_Enable
title: ScrollBar_Enable macro
author: windows-sdk-content
description: Enables or disables a scroll bar control.
old-location: controls\ScrollBar_Enable.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_enable.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ScrollBar_Enable, ScrollBar_Enable macro [Windows Controls], _win32_ScrollBar_Enable, _win32_ScrollBar_Enable_cpp, controls.ScrollBar_Enable, controls._win32_ScrollBar_Enable, windowsx/ScrollBar_Enable
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ScrollBar_Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ScrollBar_Enable macro


## -description


Enables or disables a scroll bar control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags that specify the arrows affected and whether they are enabled or disabled. See the <i>wArrows</i> parameter of <a href="https://msdn.microsoft.com/en-us/library/Bb787579(v=VS.85).aspx">EnableScrollBar</a> for more information.


## -remarks



The macro expands to a call to <a href="https://msdn.microsoft.com/en-us/library/Bb787579(v=VS.85).aspx">EnableScrollBar</a> with SB_CTL in the <i>wSBFlags</i> parameter.



