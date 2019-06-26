---
UID: NF:commctrl.ListView_SetGroupInfo
title: ListView_SetGroupInfo macro (commctrl.h)
author: windows-sdk-content
description: Sets group information. You can use this macro or send the LVM_SETGROUPINFO message explicitly.
old-location: controls\ListView_SetGroupInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setgroupinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_SetGroupInfo, ListView_SetGroupInfo macro [Windows Controls], _win32_ListView_SetGroupInfo, _win32_ListView_SetGroupInfo_cpp, commctrl/ListView_SetGroupInfo, controls.ListView_SetGroupInfo, controls._win32_ListView_SetGroupInfo
ms.topic: macro
f1_keywords: 
 - "commctrl/ListView_SetGroupInfo"
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
 - ListView_SetGroupInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetGroupInfo macro


## -description


Sets group information. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setgroupinfo">LVM_SETGROUPINFO</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param iGroupId

Type: <b>int</b>


### -param pgrp

Type: <b>PLVGROUP</b>

<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-taglvgroup">LVGROUP</a>

## -remarks



To use <b>ListView_SetGroupInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



