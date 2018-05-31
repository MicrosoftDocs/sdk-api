---
UID: NF:commctrl.ListView_GetInsertMarkRect
title: ListView_GetInsertMarkRect macro
author: windows-sdk-content
description: Gets the rectangle that bounds the insertion point. You can use this macro or send the LVM_GETINSERTMARKRECT message explicitly.
old-location: controls\ListView_GetInsertMarkRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getinsertmarkrect.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ListView_GetInsertMarkRect, ListView_GetInsertMarkRect macro [Windows Controls], _win32_ListView_GetInsertMarkRect, _win32_ListView_GetInsertMarkRect_cpp, commctrl/ListView_GetInsertMarkRect, controls.ListView_GetInsertMarkRect, controls._win32_ListView_GetInsertMarkRect
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_GetInsertMarkRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetInsertMarkRect macro


## -description


Gets the rectangle that bounds the insertion point. You can use this macro or send the <a href="https://msdn.microsoft.com/7b10229c-73ab-426c-8a8a-71258a33e248">LVM_GETINSERTMARKRECT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param rc

TBD






#### - prc

Type: <b>LPRECT</b>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>

## -remarks



To use <b>ListView_GetInsertMarkRect</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



