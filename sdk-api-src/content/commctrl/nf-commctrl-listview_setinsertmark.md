---
UID: NF:commctrl.ListView_SetInsertMark
title: ListView_SetInsertMark macro
author: windows-sdk-content
description: Sets the insertion point to the defined position. You can use this macro or send the LVM_SETINSERTMARK message explicitly.
old-location: controls\ListView_SetInsertMark.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setinsertmark.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ListView_SetInsertMark, ListView_SetInsertMark macro [Windows Controls], _win32_ListView_SetInsertMark, _win32_ListView_SetInsertMark_cpp, commctrl/ListView_SetInsertMark, controls.ListView_SetInsertMark, controls._win32_ListView_SetInsertMark
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_SetInsertMark
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetInsertMark macro


## -description


Sets the insertion point to the defined position. You can use this macro or send the <a href="https://msdn.microsoft.com/32cf5a11-918a-4dc4-bf10-88b3c26f26cc">LVM_SETINSERTMARK</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param lvim

TBD






#### - plvim

Type: <b>PLVINSERTMARK</b>

<a href="https://msdn.microsoft.com/61af07a1-34b1-4780-b36e-765e80783116">LVINSERTMARK</a>

## -remarks



To use <b>ListView_SetInsertMark</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



