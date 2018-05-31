---
UID: NF:commctrl.ListView_SetTileViewInfo
title: ListView_SetTileViewInfo macro
author: windows-sdk-content
description: Sets information that a list-view control uses in tile view. You can use this macro or send the LVM_SETTILEVIEWINFO message explicitly.
old-location: controls\ListView_SetTileViewInfo.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settileviewinfo.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ListView_SetTileViewInfo, ListView_SetTileViewInfo macro [Windows Controls], _win32_ListView_SetTileViewInfo, _win32_ListView_SetTileViewInfo_cpp, commctrl/ListView_SetTileViewInfo, controls.ListView_SetTileViewInfo, controls._win32_ListView_SetTileViewInfo
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_SetTileViewInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetTileViewInfo macro


## -description


Sets information that a list-view control uses in tile view. You can use this macro or send the <a href="https://msdn.microsoft.com/1c4f2aff-1ce1-484a-9360-3efbe870b39b">LVM_SETTILEVIEWINFO</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param ptvi

TBD






#### - plvtvinfo

Type: <b>PLVTILEVIEWINFO</b>

<a href="https://msdn.microsoft.com/5169e3bd-1805-4a19-b5f1-098c100a7625">LVTILEVIEWINFO</a>

## -remarks



To use <b>ListView_SetTileViewInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



