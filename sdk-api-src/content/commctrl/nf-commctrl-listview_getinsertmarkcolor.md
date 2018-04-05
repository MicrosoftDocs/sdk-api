---
UID: NF:commctrl.ListView_GetInsertMarkColor
title: ListView_GetInsertMarkColor macro
author: windows-driver-content
description: Gets the color of the insertion point. You can use this macro or send the LVM_GETINSERTMARKCOLOR message explicitly.
old-location: controls\ListView_GetInsertMarkColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getinsertmarkcolor.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: ListView_GetInsertMarkColor, ListView_GetInsertMarkColor macro [Windows Controls], _win32_ListView_GetInsertMarkColor, _win32_ListView_GetInsertMarkColor_cpp, commctrl/ListView_GetInsertMarkColor, controls.ListView_GetInsertMarkColor, controls._win32_ListView_GetInsertMarkColor
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_GetInsertMarkColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetInsertMarkColor macro


## -description


Gets the color of the insertion point. You can use this macro or send the <a href="https://msdn.microsoft.com/1e98023a-9d26-4b87-bee4-bee4939ccfca">LVM_GETINSERTMARKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



To use <b>ListView_GetInsertMarkColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



