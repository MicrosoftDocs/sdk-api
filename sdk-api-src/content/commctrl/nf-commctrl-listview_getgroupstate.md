---
UID: NF:commctrl.ListView_GetGroupState
title: ListView_GetGroupState macro (commctrl.h)
description: Gets the state for a specified group. Use this macro or send the LVM_GETGROUPSTATE message explicitly.helpviewer_keywords: ["ListView_GetGroupState","ListView_GetGroupState macro [Windows Controls]","_shell_ListView_GetGroupState","_shell_ListView_GetGroupState_cpp","commctrl/ListView_GetGroupState","controls.ListView_GetGroupState","controls._shell_ListView_GetGroupState"]
old-location: controls\ListView_GetGroupState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupstate.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetGroupState, ListView_GetGroupState macro [Windows Controls], _shell_ListView_GetGroupState, _shell_ListView_GetGroupState_cpp, commctrl/ListView_GetGroupState, controls.ListView_GetGroupState, controls._shell_ListView_GetGroupState
f1_keywords:
- commctrl/ListView_GetGroupState
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- ListView_GetGroupState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetGroupState macro


## -description


Gets the state for a specified group. Use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getgroupstate">LVM_GETGROUPSTATE</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.


### -param dwGroupId [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the group by <b>iGroupId</b> (see  <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a> structure).


### -param dwMask [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the state values to retrieve. This is a combination of the flags listed for the <b>state</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a>.

