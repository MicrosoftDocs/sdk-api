---
UID: NF:commctrl.ListView_SetHotCursor
title: ListView_SetHotCursor macro
author: windows-sdk-content
description: Sets the HCURSOR that the list-view control uses when the pointer is over an item while hot tracking is enabled. You can use this macro or send the LVM_SETHOTCURSOR message explicitly. To check whether hot tracking is enabled, call SystemParametersInfo.
old-location: controls\ListView_SetHotCursor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sethotcursor.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ListView_SetHotCursor, ListView_SetHotCursor macro [Windows Controls], _win32_ListView_SetHotCursor, _win32_ListView_SetHotCursor_cpp, commctrl/ListView_SetHotCursor, controls.ListView_SetHotCursor, controls._win32_ListView_SetHotCursor
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
 - ListView_SetHotCursor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetHotCursor macro


## -description


Sets the HCURSOR that the list-view control uses when the pointer is over an item while hot tracking is enabled. You can use this macro or send the <a href="https://msdn.microsoft.com/e3ff8608-9389-4167-839b-ecc2be01bb64">LVM_SETHOTCURSOR</a> message explicitly. To check whether hot tracking is enabled, call <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param hcur

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HCURSOR</a></b>

A handle to the cursor to be set. 


## -remarks



A list-view control uses hot tracking and hover selection when the <a href="Extended_list_view_styles.htm">LVS_EX_TRACKSELECT</a> style is set. 



