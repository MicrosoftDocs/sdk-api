---
UID: NF:commctrl.ListView_GetOutlineColor
title: ListView_GetOutlineColor macro
author: windows-sdk-content
description: Gets the color of the border of a list-view control if the LVS_EX_BORDERSELECT extended window style is set. You can use this macro or send the LVM_GETOUTLINECOLOR message explicitly.
old-location: controls\ListView_GetOutlineColor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getoutlinecolor.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_GetOutlineColor, ListView_GetOutlineColor macro [Windows Controls], _win32_ListView_GetOutlineColor, _win32_ListView_GetOutlineColor_cpp, commctrl/ListView_GetOutlineColor, controls.ListView_GetOutlineColor, controls._win32_ListView_GetOutlineColor
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
 - ListView_GetOutlineColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetOutlineColor macro


## -description


Gets the color of the border of a list-view control if the <a href="https://msdn.microsoft.com/en-us/library/Bb774732(v=VS.85).aspx">LVS_EX_BORDERSELECT</a> extended window style is set. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761065(v=VS.85).aspx">LVM_GETOUTLINECOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



To use <b>ListView_GetOutlineColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



