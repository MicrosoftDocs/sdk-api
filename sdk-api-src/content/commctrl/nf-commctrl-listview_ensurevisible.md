---
UID: NF:commctrl.ListView_EnsureVisible
title: ListView_EnsureVisible macro
author: windows-sdk-content
description: Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary. You can use this macro or send the LVM_ENSUREVISIBLE message explicitly.
old-location: controls\ListView_EnsureVisible.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_ensurevisible.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ListView_EnsureVisible, ListView_EnsureVisible macro [Windows Controls], _win32_ListView_EnsureVisible, _win32_ListView_EnsureVisible_cpp, commctrl/ListView_EnsureVisible, controls.ListView_EnsureVisible, controls._win32_ListView_EnsureVisible
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
 - ListView_EnsureVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_EnsureVisible macro


## -description


Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774902(v=VS.85).aspx">LVM_ENSUREVISIBLE</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param i

Type: <b>int</b>

The index of the list-view item. 


### -param fPartialOK

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

A value specifying whether the item must be entirely visible. If this parameter is <b>TRUE</b>, no scrolling occurs if the item is at least partially visible. 

