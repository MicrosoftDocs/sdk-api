---
UID: NF:commctrl.ListView_GetTileViewInfo
title: ListView_GetTileViewInfo macro
author: windows-sdk-content
description: Gets information about a list-view control in tile view. You can use this macro or send the LVM_GETTILEVIEWINFO message explicitly.
old-location: controls\ListView_GetTileViewInfo.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettileviewinfo.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ListView_GetTileViewInfo, ListView_GetTileViewInfo macro [Windows Controls], _win32_ListView_GetTileViewInfo, _win32_ListView_GetTileViewInfo_cpp, commctrl/ListView_GetTileViewInfo, controls.ListView_GetTileViewInfo, controls._win32_ListView_GetTileViewInfo
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
 - ListView_GetTileViewInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetTileViewInfo macro


## -description


Gets information about a list-view control in tile view. You can use this macro or send the <a href="https://msdn.microsoft.com/114990c0-a150-49d8-80e7-b084c648ac34">LVM_GETTILEVIEWINFO</a> message explicitly. 


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



To use <b>ListView_GetTileViewInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



