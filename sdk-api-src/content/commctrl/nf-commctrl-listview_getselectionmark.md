---
UID: NF:commctrl.ListView_GetSelectionMark
title: ListView_GetSelectionMark macro
author: windows-driver-content
description: Gets the selection mark from a list-view control. You can use this macro or explicitly send the LVM_GETSELECTIONMARK message.
old-location: controls\ListView_GetSelectionMark.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getselectionmark.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ListView_GetSelectionMark, ListView_GetSelectionMark macro [Windows Controls], _win32_ListView_GetSelectionMark, _win32_ListView_GetSelectionMark_cpp, commctrl/ListView_GetSelectionMark, controls.ListView_GetSelectionMark, controls._win32_ListView_GetSelectionMark
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_GetSelectionMark
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetSelectionMark macro


## -description


Gets the selection mark from a list-view control. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/21daf7d7-1217-4608-93f9-c390546f1591">LVM_GETSELECTIONMARK</a> message. 


## -parameters




### -param hwnd

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


## -remarks



The selection mark is the item index from which a multiple selection starts. 




## -see-also




<a href="https://msdn.microsoft.com/75cb06d0-3d6f-4523-b912-3c12e368f17e">ListView_SetSelectionMark</a>
 

 

