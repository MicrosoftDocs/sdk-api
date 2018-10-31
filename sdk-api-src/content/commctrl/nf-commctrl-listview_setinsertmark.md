---
UID: NF:commctrl.ListView_SetInsertMark
title: ListView_SetInsertMark macro
author: windows-sdk-content
description: Sets the insertion point to the defined position. You can use this macro or send the LVM_SETINSERTMARK message explicitly.
old-location: controls\ListView_SetInsertMark.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setinsertmark.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ListView_SetInsertMark, ListView_SetInsertMark macro [Windows Controls], _win32_ListView_SetInsertMark, _win32_ListView_SetInsertMark_cpp, commctrl/ListView_SetInsertMark, controls.ListView_SetInsertMark, controls._win32_ListView_SetInsertMark
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
 - ListView_SetInsertMark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetInsertMark macro


## -description


Sets the insertion point to the defined position. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761182(v=VS.85).aspx">LVM_SETINSERTMARK</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param lvim

Type: <b>PLVINSERTMARK</b>

<a href="https://msdn.microsoft.com/en-us/library/Bb774758(v=VS.85).aspx">LVINSERTMARK</a>

## -remarks



To use <b>ListView_SetInsertMark</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



