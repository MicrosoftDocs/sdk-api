---
UID: NF:commctrl.ListView_GetSelectedCount
title: ListView_GetSelectedCount macro
author: windows-sdk-content
description: Determines the number of selected items in a list-view control. You can use this macro or send the LVM_GETSELECTEDCOUNT message explicitly.
old-location: controls\ListView_GetSelectedCount.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getselectedcount.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ListView_GetSelectedCount, ListView_GetSelectedCount macro [Windows Controls], _win32_ListView_GetSelectedCount, _win32_ListView_GetSelectedCount_cpp, commctrl/ListView_GetSelectedCount, controls.ListView_GetSelectedCount, controls._win32_ListView_GetSelectedCount
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
 - ListView_GetSelectedCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetSelectedCount macro


## -description


Determines the number of selected items in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/38916227-e6ca-4efa-9821-13f0fdb29834">LVM_GETSELECTEDCOUNT</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 

