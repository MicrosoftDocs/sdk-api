---
UID: NF:commctrl.ListView_GetSelectionMark
title: ListView_GetSelectionMark macro
author: windows-sdk-content
description: Gets the selection mark from a list-view control. You can use this macro or explicitly send the LVM_GETSELECTIONMARK message.
old-location: controls\ListView_GetSelectionMark.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getselectionmark.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetSelectionMark macro


## -description


Gets the selection mark from a list-view control. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/en-us/library/Bb761071(v=VS.85).aspx">LVM_GETSELECTIONMARK</a> message. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to a list-view control. 


## -remarks



The selection mark is the item index from which a multiple selection starts. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775112(v=VS.85).aspx">ListView_SetSelectionMark</a>
 

 

