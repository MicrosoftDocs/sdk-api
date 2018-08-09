---
UID: NF:commctrl.ListView_SetTileInfo
title: ListView_SetTileInfo macro
author: windows-sdk-content
description: Sets information for an existing tile of a list-view control. You can use this macro or send the LVM_SETTILEINFO message explicitly.
old-location: controls\ListView_SetTileInfo.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settileinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_SetTileInfo, ListView_SetTileInfo macro [Windows Controls], _win32_ListView_SetTileInfo, _win32_ListView_SetTileInfo_cpp, commctrl/ListView_SetTileInfo, controls.ListView_SetTileInfo, controls._win32_ListView_SetTileInfo
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
 - ListView_SetTileInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetTileInfo macro


## -description


Sets information for an existing tile of a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/345e8f16-9a6c-44e3-a262-d5d3be4d33ef">LVM_SETTILEINFO</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pti

Type: <b>PLVTILEINFO</b>

<a href="https://msdn.microsoft.com/bb8ab1e8-91bc-46e5-827c-c24665bf63d7">LVTILEINFO</a>

## -remarks



To use <b>ListView_SetTileInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



