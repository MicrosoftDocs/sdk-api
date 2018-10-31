---
UID: NF:commctrl.ListView_DeleteItem
title: ListView_DeleteItem macro
author: windows-sdk-content
description: Removes an item from a list-view control. You can use this macro or send the LVM_DELETEITEM message explicitly.
old-location: controls\ListView_DeleteItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_deleteitem.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ListView_DeleteItem, ListView_DeleteItem macro [Windows Controls], _win32_ListView_DeleteItem, _win32_ListView_DeleteItem_cpp, commctrl/ListView_DeleteItem, controls.ListView_DeleteItem, controls._win32_ListView_DeleteItem
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
 - ListView_DeleteItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_DeleteItem macro


## -description


Removes an item from a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/0eddd4c1-7786-4a8c-a16d-9fd83cce98b3">LVM_DELETEITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param i

Type: <b>int</b>

An index of the list-view item to delete. 

