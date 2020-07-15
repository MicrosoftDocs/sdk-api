---
UID: NF:commctrl.ListView_CancelEditLabel
title: ListView_CancelEditLabel macro (commctrl.h)
description: Cancels an item text editing operation. You can use this macro or send the LVM_CANCELEDITLABEL message explicitly.
helpviewer_keywords: ["ListView_CancelEditLabel","ListView_CancelEditLabel macro [Windows Controls]","_win32_ListView_CancelEditLabel","_win32_ListView_CancelEditLabel_cpp","commctrl/ListView_CancelEditLabel","controls.ListView_CancelEditLabel","controls._win32_ListView_CancelEditLabel"]
old-location: controls\ListView_CancelEditLabel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_canceleditlabel.htm
ms.date: 12/05/2018
ms.keywords: ListView_CancelEditLabel, ListView_CancelEditLabel macro [Windows Controls], _win32_ListView_CancelEditLabel, _win32_ListView_CancelEditLabel_cpp, commctrl/ListView_CancelEditLabel, controls.ListView_CancelEditLabel, controls._win32_ListView_CancelEditLabel
f1_keywords:
- commctrl/ListView_CancelEditLabel
dev_langs:
- c++
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
- ListView_CancelEditLabel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_CancelEditLabel macro


## -description


Cancels an item text editing operation. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-canceleditlabel">LVM_CANCELEDITLABEL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


## -remarks



To use <b>ListView_CancelEditLabel</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



