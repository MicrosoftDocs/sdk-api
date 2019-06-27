---
UID: NF:commctrl.ListView_SetView
title: ListView_SetView macro (commctrl.h)
author: windows-sdk-content
description: Sets the view of a list-view control. You can use this macro or send the LVM_SETVIEW message explicitly.
old-location: controls\ListView_SetView.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setview.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_SetView, ListView_SetView macro [Windows Controls], _win32_ListView_SetView, _win32_ListView_SetView_cpp, commctrl/ListView_SetView, controls.ListView_SetView, controls._win32_ListView_SetView
ms.topic: macro
f1_keywords: 
 - "commctrl/ListView_SetView"
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
 - ListView_SetView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetView macro


## -description


Sets the view of a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setview">LVM_SETVIEW</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param iView

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b>
<a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setview">LVM_SETVIEW</a>

## -remarks



To use <b>ListView_SetView</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



