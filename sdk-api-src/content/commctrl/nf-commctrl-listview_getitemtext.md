---
UID: NF:commctrl.ListView_GetItemText
title: ListView_GetItemText macro
author: windows-sdk-content
description: Gets the text of a list-view item or subitem. You can use this macro or send the LVM_GETITEMTEXT message explicitly.
old-location: controls\ListView_GetItemText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemtext.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ListView_GetItemText, ListView_GetItemText macro [Windows Controls], _win32_ListView_GetItemText, _win32_ListView_GetItemText_cpp, commctrl/ListView_GetItemText, controls.ListView_GetItemText, controls._win32_ListView_GetItemText
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
 - ListView_GetItemText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetItemText macro


## -description


Gets the text of a list-view item or subitem. You can use this macro or send the <a href="https://msdn.microsoft.com/5711ed18-a766-4e7f-9e9d-b9203231b369">LVM_GETITEMTEXT</a> message explicitly.


## -parameters




### -param hwndLV

TBD


### -param i

TBD


#### - iSubItem_

Type: <b>int</b>

The index of the subitem. To retrieve the item text, set 
					<i>iSubItem</i> to zero. 


#### - pszText_

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a buffer that receives the item or subitem text. 


#### - cchTextMax_

Type: <b>int</b>

The number of characters in the 
					<i>pszText</i> buffer.


#### - cchTextMax

Type: <b>int</b>

The number of characters in the 
					<i>pszText</i> buffer.


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - iItem

Type: <b>int</b>

The index of the list-view item. 


#### - iSubItem

Type: <b>int</b>

The index of the subitem. To retrieve the item text, set 
					<i>iSubItem</i> to zero. 


#### - pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a buffer that receives the item or subitem text. 


## -see-also




<a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a>
 

 

