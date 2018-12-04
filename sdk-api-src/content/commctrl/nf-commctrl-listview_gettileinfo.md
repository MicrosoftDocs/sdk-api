---
UID: NF:commctrl.ListView_GetTileInfo
title: ListView_GetTileInfo macro
author: windows-sdk-content
description: Gets information about a tile in a list-view control. You can use this macro or send the LVM_GETTILEINFO message explicitly.
old-location: controls\ListView_GetTileInfo.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettileinfo.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ListView_GetTileInfo, ListView_GetTileInfo macro [Windows Controls], _win32_ListView_GetTileInfo, _win32_ListView_GetTileInfo_cpp, commctrl/ListView_GetTileInfo, controls.ListView_GetTileInfo, controls._win32_ListView_GetTileInfo
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
 - ListView_GetTileInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetTileInfo macro


## -description


Gets information about a tile in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/e89a3eae-0970-488c-ba95-1072aa85bbf4">LVM_GETTILEINFO</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pti

Type: <b>PLVTILEINFO</b>

<a href="https://msdn.microsoft.com/bb8ab1e8-91bc-46e5-827c-c24665bf63d7">LVTILEINFO</a>

## -remarks



To use <b>ListView_GetTileInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



