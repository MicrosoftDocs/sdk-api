---
UID: NF:commctrl.ListView_GetGroupInfo
title: ListView_GetGroupInfo macro (commctrl.h)
description: Gets group information. You can use this macro or send the LVM_GETGROUPINFO message explicitly.
helpviewer_keywords: ["ListView_GetGroupInfo","ListView_GetGroupInfo macro [Windows Controls]","_win32_ListView_GetGroupInfo","_win32_ListView_GetGroupInfo_cpp","commctrl/ListView_GetGroupInfo","controls.ListView_GetGroupInfo","controls._win32_ListView_GetGroupInfo"]
old-location: controls\ListView_GetGroupInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupinfo.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetGroupInfo, ListView_GetGroupInfo macro [Windows Controls], _win32_ListView_GetGroupInfo, _win32_ListView_GetGroupInfo_cpp, commctrl/ListView_GetGroupInfo, controls.ListView_GetGroupInfo, controls._win32_ListView_GetGroupInfo
f1_keywords:
- commctrl/ListView_GetGroupInfo
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
- ListView_GetGroupInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetGroupInfo macro


## -description


Gets group information. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getgroupinfo">LVM_GETGROUPINFO</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param iGroupId

Type: <b>int</b>


### -param pgrp

Type: <b>PLVGROUP</b>

<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a>

## -remarks



To use <b>ListView_GetGroupInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



