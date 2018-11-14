---
UID: NF:commctrl.ListView_GetInsertMark
title: ListView_GetInsertMark macro
author: windows-sdk-content
description: Gets the position of the insertion point. You can use this macro or send the LVM_GETINSERTMARK message explicitly.
old-location: controls\ListView_GetInsertMark.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getinsertmark.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_GetInsertMark, ListView_GetInsertMark macro [Windows Controls], _win32_ListView_GetInsertMark, _win32_ListView_GetInsertMark_cpp, commctrl/ListView_GetInsertMark, controls.ListView_GetInsertMark, controls._win32_ListView_GetInsertMark
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
 - ListView_GetInsertMark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- ListView_GetInsertMark
: 
---

# ListView_GetInsertMark macro


## -description


Gets the position of the insertion point. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774945(v=VS.85).aspx">LVM_GETINSERTMARK</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param lvim

Type: <b>PLVINSERTMARK</b>

<a href="https://msdn.microsoft.com/en-us/library/Bb774758(v=VS.85).aspx">LVINSERTMARK</a>

## -remarks



To use <b>ListView_GetInsertMark</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



