---
UID: NF:commctrl.ListView_GetSelectedColumn
title: ListView_GetSelectedColumn macro
author: windows-sdk-content
description: Gets an integer that specifies the selected column. You can use this macro or send the LVM_GETSELECTEDCOLUMN message explicitly.
old-location: controls\ListView_GetSelectedColumn.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getselectedcolumn.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ListView_GetSelectedColumn, ListView_GetSelectedColumn macro [Windows Controls], _win32_ListView_GetSelectedColumn, _win32_ListView_GetSelectedColumn_cpp, commctrl/ListView_GetSelectedColumn, controls.ListView_GetSelectedColumn, controls._win32_ListView_GetSelectedColumn
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
 - ListView_GetSelectedColumn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetSelectedColumn macro


## -description


Gets an integer that specifies the selected column. You can use this macro or send the <a href="https://msdn.microsoft.com/5aba5d96-50fd-439b-9782-fd5d8684b17f">LVM_GETSELECTEDCOLUMN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



To use <b>ListView_GetSelectedColumn</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



