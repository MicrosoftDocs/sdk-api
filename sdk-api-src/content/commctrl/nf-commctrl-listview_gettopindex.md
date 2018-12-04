---
UID: NF:commctrl.ListView_GetTopIndex
title: ListView_GetTopIndex macro
author: windows-sdk-content
description: Gets the index of the topmost visible item when in list or report view. You can use this macro or send the LVM_GETTOPINDEX message explicitly.
old-location: controls\ListView_GetTopIndex.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettopindex.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ListView_GetTopIndex, ListView_GetTopIndex macro [Windows Controls], _win32_ListView_GetTopIndex, _win32_ListView_GetTopIndex_cpp, commctrl/ListView_GetTopIndex, controls.ListView_GetTopIndex, controls._win32_ListView_GetTopIndex
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
 - ListView_GetTopIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetTopIndex macro


## -description


Gets the index of the topmost visible item when in list or report view. You can use this macro or send the <a href="https://msdn.microsoft.com/b5692de3-338b-422c-9dee-d3ba96f2b53d">LVM_GETTOPINDEX</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 

