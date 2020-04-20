---
UID: NF:commctrl.ListView_GetSelectionMark
title: ListView_GetSelectionMark macro (commctrl.h)
description: Gets the selection mark from a list-view control. You can use this macro or explicitly send the LVM_GETSELECTIONMARK message.helpviewer_keywords: ["ListView_GetSelectionMark","ListView_GetSelectionMark macro [Windows Controls]","_win32_ListView_GetSelectionMark","_win32_ListView_GetSelectionMark_cpp","commctrl/ListView_GetSelectionMark","controls.ListView_GetSelectionMark","controls._win32_ListView_GetSelectionMark"]
old-location: controls\ListView_GetSelectionMark.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getselectionmark.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetSelectionMark, ListView_GetSelectionMark macro [Windows Controls], _win32_ListView_GetSelectionMark, _win32_ListView_GetSelectionMark_cpp, commctrl/ListView_GetSelectionMark, controls.ListView_GetSelectionMark, controls._win32_ListView_GetSelectionMark
f1_keywords:
- commctrl/ListView_GetSelectionMark
dev_langs:
- c++
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
- ListView_GetSelectionMark
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetSelectionMark macro


## -description


Gets the selection mark from a list-view control. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getselectionmark">LVM_GETSELECTIONMARK</a> message. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control. 


## -remarks



The selection mark is the item index from which a multiple selection starts. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_setselectionmark">ListView_SetSelectionMark</a>
 

 

