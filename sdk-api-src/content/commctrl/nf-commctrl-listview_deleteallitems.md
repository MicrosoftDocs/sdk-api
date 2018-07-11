---
UID: NF:commctrl.ListView_DeleteAllItems
title: ListView_DeleteAllItems macro
author: windows-sdk-content
description: Removes all items from a list-view control. You can use this macro or send the LVM_DELETEALLITEMS message explicitly.
old-location: controls\ListView_DeleteAllItems.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_deleteallitems.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ListView_DeleteAllItems, ListView_DeleteAllItems macro [Windows Controls], _win32_ListView_DeleteAllItems, _win32_ListView_DeleteAllItems_cpp, commctrl/ListView_DeleteAllItems, controls.ListView_DeleteAllItems, controls._win32_ListView_DeleteAllItems
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
 - ListView_DeleteAllItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_DeleteAllItems macro


## -description


Removes all items from a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb774891(v=VS.85).aspx">LVM_DELETEALLITEMS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



When a list-view control receives the <a href="https://msdn.microsoft.com/library/Bb774891(v=VS.85).aspx">LVM_DELETEALLITEMS</a> message, it sends the <a href="https://msdn.microsoft.com/library/Bb774810(v=VS.85).aspx">LVN_DELETEALLITEMS</a> notification code to its parent window. 



