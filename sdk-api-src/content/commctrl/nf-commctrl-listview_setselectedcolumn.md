---
UID: NF:commctrl.ListView_SetSelectedColumn
title: ListView_SetSelectedColumn macro
author: windows-sdk-content
description: Sets the index of the selected column. You can use this macro or send the LVM_SETSELECTEDCOLUMN message explicitly.
old-location: controls\ListView_SetSelectedColumn.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setselectedcolumn.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ListView_SetSelectedColumn, ListView_SetSelectedColumn macro [Windows Controls], _win32_ListView_SetSelectedColumn, _win32_ListView_SetSelectedColumn_cpp, commctrl/ListView_SetSelectedColumn, controls.ListView_SetSelectedColumn, controls._win32_ListView_SetSelectedColumn
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
 - ListView_SetSelectedColumn
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetSelectedColumn macro


## -description


Sets the index of the selected column. You can use this macro or send the <a href="https://msdn.microsoft.com/11b0838e-24a7-4c1c-b67d-0912b5a6442a">LVM_SETSELECTEDCOLUMN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param iCol

Type: <b>int</b>

<b>int</b>

## -remarks



To use <b>ListView_SetSelectedColumn</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



