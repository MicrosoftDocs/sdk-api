---
UID: NF:commctrl.ListView_GetItemText
title: ListView_GetItemText macro
author: windows-sdk-content
description: Gets the text of a list-view item or subitem. You can use this macro or send the LVM_GETITEMTEXT message explicitly.
old-location: controls\ListView_GetItemText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemtext.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ListView_GetItemText, ListView_GetItemText macro [Windows Controls], _win32_ListView_GetItemText, _win32_ListView_GetItemText_cpp, commctrl/ListView_GetItemText, controls.ListView_GetItemText, controls._win32_ListView_GetItemText
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
 - ListView_GetItemText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetItemText macro


## -description


Gets the text of a list-view item or subitem. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761055(v=VS.85).aspx">LVM_GETITEMTEXT</a> message explicitly.


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param i

Type: <b>int</b>

The index of the list-view item. 


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


#### - iSubItem

Type: <b>int</b>

The index of the subitem. To retrieve the item text, set 
					<i>iSubItem</i> to zero. 


#### - pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a buffer that receives the item or subitem text. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774760(v=VS.85).aspx">LVITEM</a>
 

 

