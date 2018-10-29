---
UID: NF:commctrl.ListView_SetInsertMarkColor
title: ListView_SetInsertMarkColor macro
author: windows-sdk-content
description: Sets the color of the insertion point. You can use this macro or send the LVM_SETINSERTMARKCOLOR message explicitly.
old-location: controls\ListView_SetInsertMarkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setinsertmarkcolor.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ListView_SetInsertMarkColor, ListView_SetInsertMarkColor macro [Windows Controls], _win32_ListView_SetInsertMarkColor, _win32_ListView_SetInsertMarkColor_cpp, commctrl/ListView_SetInsertMarkColor, controls.ListView_SetInsertMarkColor, controls._win32_ListView_SetInsertMarkColor
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
 - ListView_SetInsertMarkColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetInsertMarkColor macro


## -description


Sets the color of the insertion point. You can use this macro or send the <a href="https://msdn.microsoft.com/dce2c266-672b-4682-ba23-51d9a8e1102b">LVM_SETINSERTMARKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param color

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b>

## -remarks



To use <b>ListView_SetInsertMarkColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



