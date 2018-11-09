---
UID: NF:commctrl.ListView_GetItem
title: ListView_GetItem macro
author: windows-sdk-content
description: Gets some or all of a list-view item's attributes. You can use this macro or send the LVM_GETITEM message explicitly.
old-location: controls\ListView_GetItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitem.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_GetItem, ListView_GetItem macro [Windows Controls], _win32_ListView_GetItem, _win32_ListView_GetItem_cpp, commctrl/ListView_GetItem, controls.ListView_GetItem, controls._win32_ListView_GetItem
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
 - ListView_GetItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetItem macro


## -description


Gets some or all of a list-view item's attributes. You can use this macro or send the <a href="https://msdn.microsoft.com/684ad96a-2c3b-4148-b66c-41f8322500bb">LVM_GETITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pitem

Type: <b>LPLVITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure that specifies the information to retrieve and receives information about the list-view item. 


## -remarks



When the <a href="https://msdn.microsoft.com/684ad96a-2c3b-4148-b66c-41f8322500bb">LVM_GETITEM</a> message is sent, the 
				<b>iItem</b> and <b>iSubItem</b> members identify the item or subitem to retrieve information about and the <b>mask</b> member specifies which attributes to retrieve. For a list of possible values, see the description of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure.

If the LVIF_TEXT flag is set in the <b>mask</b> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure, the <b>pszText</b> member must point to a valid buffer and the <b>cchTextMax</b> member must be set to the number of characters in that buffer. Applications should not assume that the text will necessarily be placed in the specified buffer. The control may instead change the <b>pszText</b> member of the structure to point to the new text rather than place it in the buffer.

If the <b>mask</b> member specifies the LVIF_STATE value, the <b>stateMask</b> member must specify the item state bits to retrieve. On output, the <b>state</b> member contains the values of the specified state bits.



