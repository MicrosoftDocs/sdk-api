---
UID: NF:commctrl.ListView_SetOutlineColor
title: ListView_SetOutlineColor macro
author: windows-sdk-content
description: Sets the color of the border of a list-view control if the LVS_EX_BORDERSELECT extended window style is set. You can use this macro or send the LVM_SETOUTLINECOLOR message explicitly.
old-location: controls\ListView_SetOutlineColor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setoutlinecolor.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_SetOutlineColor, ListView_SetOutlineColor macro [Windows Controls], _win32_ListView_SetOutlineColor, _win32_ListView_SetOutlineColor_cpp, commctrl/ListView_SetOutlineColor, controls.ListView_SetOutlineColor, controls._win32_ListView_SetOutlineColor
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
 - ListView_SetOutlineColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetOutlineColor macro


## -description


Sets the color of the border of a list-view control if the <a href="https://msdn.microsoft.com/en-us/library/Bb774732(v=VS.85).aspx">LVS_EX_BORDERSELECT</a> extended window style is set. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761200(v=VS.85).aspx">LVM_SETOUTLINECOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param color

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b>

## -remarks



To use <b>ListView_SetOutlineColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



