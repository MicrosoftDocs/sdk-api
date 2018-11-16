---
UID: NF:commctrl.ListView_EditLabel
title: ListView_EditLabel macro
author: windows-sdk-content
description: Begins in-place editing of the specified list-view item's text. The message implicitly selects and focuses the specified item. You can use this macro or send the LVM_EDITLABEL message explicitly.
old-location: controls\ListView_EditLabel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_editlabel.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ListView_EditLabel, ListView_EditLabel macro [Windows Controls], _win32_ListView_EditLabel, _win32_ListView_EditLabel_cpp, commctrl/ListView_EditLabel, controls.ListView_EditLabel, controls._win32_ListView_EditLabel
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
 - ListView_EditLabel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- ListView_EditLabel
: 
---

# ListView_EditLabel macro


## -description


Begins in-place editing of the specified list-view item's text. The message implicitly selects and focuses the specified item. You can use this macro or send the <a href="https://msdn.microsoft.com/b63f13f1-6e66-4770-af84-30bcdb241727">LVM_EDITLABEL</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param i

Type: <b>int</b>

The index of the list-view item. To cancel editing, set 
					<i>iItem</i> to -1. 


## -remarks



When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid. You can subclass the edit control, but you should not destroy it. 

The control must have the focus before you send this message to the control. Focus can be set using the <a href="https://msdn.microsoft.com/88fc2959-007a-441d-8a02-19d775f28de9">SetFocus</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/c801233a-c4d8-4fd9-aaf0-3d4503bbce26">WM_CANCELMODE</a>
 

 

