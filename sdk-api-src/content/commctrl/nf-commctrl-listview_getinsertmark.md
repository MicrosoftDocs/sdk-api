---
UID: NF:commctrl.ListView_GetInsertMark
title: ListView_GetInsertMark macro
author: windows-sdk-content
description: Gets the position of the insertion point. You can use this macro or send the LVM_GETINSERTMARK message explicitly.
old-location: controls\ListView_GetInsertMark.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getinsertmark.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ListView_GetInsertMark, ListView_GetInsertMark macro [Windows Controls], _win32_ListView_GetInsertMark, _win32_ListView_GetInsertMark_cpp, commctrl/ListView_GetInsertMark, controls.ListView_GetInsertMark, controls._win32_ListView_GetInsertMark
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
 - ListView_GetInsertMark
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetInsertMark macro


## -description


Gets the position of the insertion point. You can use this macro or send the <a href="https://msdn.microsoft.com/ad00df4c-4b4b-48f1-8821-7849a216df2e">LVM_GETINSERTMARK</a> message explicitly. 


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



To use <b>ListView_GetInsertMark</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



