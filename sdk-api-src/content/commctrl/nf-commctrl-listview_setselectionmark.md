---
UID: NF:commctrl.ListView_SetSelectionMark
title: ListView_SetSelectionMark macro
author: windows-sdk-content
description: Sets the selection mark in a list-view control. You can use this macro or send the LVM_SETSELECTIONMARK message explicitly.
old-location: controls\ListView_SetSelectionMark.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setselectionmark.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ListView_SetSelectionMark, ListView_SetSelectionMark macro [Windows Controls], _win32_ListView_SetSelectionMark, _win32_ListView_SetSelectionMark_cpp, commctrl/ListView_SetSelectionMark, controls.ListView_SetSelectionMark, controls._win32_ListView_SetSelectionMark
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
 - ListView_SetSelectionMark
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetSelectionMark macro


## -description


Sets the selection mark in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/3218f1b3-b934-4083-aaaa-e10ef1dbb6bd">LVM_SETSELECTIONMARK</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param i

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


#### - iIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

the zero-based index of the list-view item to be selected. 


## -remarks



The selection mark is the item index from which a multiple selection starts. This macro does not affect the selection state of the item. 




## -see-also




<a href="https://msdn.microsoft.com/dba2484c-c938-4123-be28-35a504dd9e5a">ListView_GetSelectionMark</a>
 

 

