---
UID: NF:commctrl.ListView_SetSelectionMark
title: ListView_SetSelectionMark macro
author: windows-sdk-content
description: Sets the selection mark in a list-view control. You can use this macro or send the LVM_SETSELECTIONMARK message explicitly.
old-location: controls\ListView_SetSelectionMark.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setselectionmark.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_SetSelectionMark, ListView_SetSelectionMark macro [Windows Controls], _win32_ListView_SetSelectionMark, _win32_ListView_SetSelectionMark_cpp, commctrl/ListView_SetSelectionMark, controls.ListView_SetSelectionMark, controls._win32_ListView_SetSelectionMark
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
 - ListView_SetSelectionMark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetSelectionMark macro


## -description


Sets the selection mark in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761204(v=VS.85).aspx">LVM_SETSELECTIONMARK</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param i

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

the zero-based index of the list-view item to be selected. 


## -remarks



The selection mark is the item index from which a multiple selection starts. This macro does not affect the selection state of the item. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774998(v=VS.85).aspx">ListView_GetSelectionMark</a>
 

 

