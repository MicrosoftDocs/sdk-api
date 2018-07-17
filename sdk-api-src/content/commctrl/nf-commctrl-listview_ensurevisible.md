---
UID: NF:commctrl.ListView_EnsureVisible
title: ListView_EnsureVisible macro
author: windows-sdk-content
description: Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary. You can use this macro or send the LVM_ENSUREVISIBLE message explicitly.
old-location: controls\ListView_EnsureVisible.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_ensurevisible.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ListView_EnsureVisible, ListView_EnsureVisible macro [Windows Controls], _win32_ListView_EnsureVisible, _win32_ListView_EnsureVisible_cpp, commctrl/ListView_EnsureVisible, controls.ListView_EnsureVisible, controls._win32_ListView_EnsureVisible
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
 - ListView_EnsureVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_EnsureVisible macro


## -description


Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary. You can use this macro or send the <a href="https://msdn.microsoft.com/3564b6e6-b8b6-401b-85bc-8bd6261fc054">LVM_ENSUREVISIBLE</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param i

Type: <b>int</b>

The index of the list-view item. 


### -param fPartialOK

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A value specifying whether the item must be entirely visible. If this parameter is <b>TRUE</b>, no scrolling occurs if the item is at least partially visible. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 

