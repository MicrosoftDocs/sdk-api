---
UID: NF:commctrl.ListView_SetHoverTime
title: ListView_SetHoverTime macro
author: windows-sdk-content
description: Sets the amount of time that the mouse cursor must hover over an item before it is selected. You can use this macro or send the LVM_SETHOVERTIME message explicitly.
old-location: controls\ListView_SetHoverTime.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sethovertime.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_SetHoverTime, ListView_SetHoverTime macro [Windows Controls], _win32_ListView_SetHoverTime, _win32_ListView_SetHoverTime_cpp, commctrl/ListView_SetHoverTime, controls.ListView_SetHoverTime, controls._win32_ListView_SetHoverTime
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
 - ListView_SetHoverTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetHoverTime macro


## -description


Sets the amount of time that the mouse cursor must hover over an item before it is selected. You can use this macro or send the <a href="https://msdn.microsoft.com/454fbc38-f7fd-4dea-b223-56003b88528f">LVM_SETHOVERTIME</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param dwHoverTimeMs

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected. If this value is (<b>DWORD</b>)-1, then the hover time is set to the default hover time. 


## -remarks



The hover time only affects list-view controls that have the <a href="Extended_list_view_styles.htm">LVS_EX_TRACKSELECT</a>, <a href="Extended_list_view_styles.htm">LVS_EX_ONECLICKACTIVATE</a>, or <a href="Extended_list_view_styles.htm">LVS_EX_TWOCLICKACTIVATE</a> extended list-view style. 



