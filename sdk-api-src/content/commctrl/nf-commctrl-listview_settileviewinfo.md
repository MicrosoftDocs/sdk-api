---
UID: NF:commctrl.ListView_SetTileViewInfo
title: ListView_SetTileViewInfo macro (commctrl.h)
author: windows-sdk-content
description: Sets information that a list-view control uses in tile view. You can use this macro or send the LVM_SETTILEVIEWINFO message explicitly.
old-location: controls\ListView_SetTileViewInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settileviewinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_SetTileViewInfo, ListView_SetTileViewInfo macro [Windows Controls], _win32_ListView_SetTileViewInfo, _win32_ListView_SetTileViewInfo_cpp, commctrl/ListView_SetTileViewInfo, controls.ListView_SetTileViewInfo, controls._win32_ListView_SetTileViewInfo
ms.topic: macro
f1_keywords: ["commctrl/ListView_SetTileViewInfo"]
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
 - ListView_SetTileViewInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetTileViewInfo macro


## -description


Sets information that a list-view control uses in tile view. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-settileviewinfo">LVM_SETTILEVIEWINFO</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param ptvi

Type: <b>PLVTILEVIEWINFO</b>

<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-taglvtileviewinfo">LVTILEVIEWINFO</a>

## -remarks



To use <b>ListView_SetTileViewInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



